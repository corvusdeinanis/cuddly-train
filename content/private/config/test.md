<% moment().add(15-(moment().minute()%15),'minutes').startOf('minute').format('HH:mm') %>
 <% moment().add(15-(moment().minute()%15),'minutes').startOf('minute').add(15, 'minutes').format('HH:mm') %>
 <% moment().add(15-(moment().minute()%15),'minutes').startOf('minute').add(30, 'minutes').format('HH:mm') %>