<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Todo Card</title>
<style>
  body {
    font-family: Arial, sans-serif;
    background:#f4f4f4;
    display: flex;
    justify-content: center;
    padding: 20px;
  }
  article {
    background: white;
    padding: 20px;
    max-width: 450px;
    width: 100%;
    border-radius: 10px;
  }
  h2 {
    margin: 0;
  }
  #checkbox:checked ~ h2 {
    text-decoration: line-through;
    color: gray;
  }
  #checkbox:checked ~ #status {
    content: "Done";
  }
  .badge {
    padding: 5px 10px;
    border-radius: 5px;
    font-size: 12px;
  }
  .high {
    background: red;
    color: white;
  }

  .tags {
    display: flex;
    flex-wrap: wrap;
    gap: 5px;
    margin-top: 10px;
  }

  .tag {
    background: #ddd;
    padding: 5px 10px;
    border-radius: 20px;
  }

  button {
    margin-top: 10px;
    padding: 8px;
  }
</style>
</head>

<body>

<article data-testid="test-todo-card">
  <label>
    <input type="checkbox" id="checkbox" data-testid="test-todo-complete-toggle">
    Mark as complete
  </label>
  <h2 data-testid="test-todo-title">Finish HTML Assignment</h2>
  <p data-testid="test-todo-description">
    Complete the todo card project and submit before deadline.
  </p>

  <span class="badge high" data-testid="test-todo-priority">High </span>
  <span id="status" data-testid="test-todo-status">Pending</span>
  <br><br>

  <time data-testid="test-todo-due-date" datetime="2026-03-01">Due March 1, 2026
  </time>

  <br>
  <time data-testid="test-todo-time-remaining">
    Due in 3 days
  </time>
  <div class="tags" data-testid="test-todo-tags">
    <span class="tag" data-testid="test-todo-tag-work">Work</span>
    <span class="tag" data-testid="test-todo-tag-urgent">Urgent</span>
  </div>


  <button data-testid="test-todo-edit-button">
    Edit
  </button>

  <button data-testid="test-todo-delete-button">
    Delete
  </button>

</article>

</body>
</html>
