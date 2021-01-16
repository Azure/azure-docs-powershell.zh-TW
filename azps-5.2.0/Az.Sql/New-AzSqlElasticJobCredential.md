---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobCredential.md
ms.openlocfilehash: 404b34c7e0d169e1d123a5c1ded8e6b5bef2fe2e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98283495"
---
# <span data-ttu-id="56976-101">New-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="56976-101">New-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="56976-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56976-102">SYNOPSIS</span></span>
<span data-ttu-id="56976-103">建立新的作業認證</span><span class="sxs-lookup"><span data-stu-id="56976-103">Creates a new job credential</span></span>

## <span data-ttu-id="56976-104">句法</span><span class="sxs-lookup"><span data-stu-id="56976-104">SYNTAX</span></span>

### <span data-ttu-id="56976-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="56976-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56976-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="56976-106">ObjectSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56976-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="56976-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56976-108">說明</span><span class="sxs-lookup"><span data-stu-id="56976-108">DESCRIPTION</span></span>
<span data-ttu-id="56976-109">New-AzSqlElasticJobCredential Cmdlet 會建立新的作業認證</span><span class="sxs-lookup"><span data-stu-id="56976-109">The New-AzSqlElasticJobCredential cmdlet creates a new job credential</span></span>

## <span data-ttu-id="56976-110">示例</span><span class="sxs-lookup"><span data-stu-id="56976-110">EXAMPLES</span></span>

### <span data-ttu-id="56976-111">範例1</span><span class="sxs-lookup"><span data-stu-id="56976-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="56976-112">建立新的作業認證</span><span class="sxs-lookup"><span data-stu-id="56976-112">Creates a new job credential</span></span>

## <span data-ttu-id="56976-113">參數</span><span class="sxs-lookup"><span data-stu-id="56976-113">PARAMETERS</span></span>

### <span data-ttu-id="56976-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="56976-114">-AgentName</span></span>
<span data-ttu-id="56976-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="56976-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56976-116">-認證</span><span class="sxs-lookup"><span data-stu-id="56976-116">-Credential</span></span>
<span data-ttu-id="56976-117">認證</span><span class="sxs-lookup"><span data-stu-id="56976-117">The credential</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56976-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56976-118">-DefaultProfile</span></span>
<span data-ttu-id="56976-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56976-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56976-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="56976-120">-Name</span></span>
<span data-ttu-id="56976-121">作業認證名稱</span><span class="sxs-lookup"><span data-stu-id="56976-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56976-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="56976-122">-ParentObject</span></span>
<span data-ttu-id="56976-123">Agent 物件</span><span class="sxs-lookup"><span data-stu-id="56976-123">The agent object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56976-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="56976-124">-ParentResourceId</span></span>
<span data-ttu-id="56976-125">Agent 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="56976-125">The agent resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56976-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56976-126">-ResourceGroupName</span></span>
<span data-ttu-id="56976-127">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="56976-127">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56976-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56976-128">-ServerName</span></span>
<span data-ttu-id="56976-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="56976-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56976-130">-確認</span><span class="sxs-lookup"><span data-stu-id="56976-130">-Confirm</span></span>
<span data-ttu-id="56976-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="56976-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56976-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56976-132">-WhatIf</span></span>
<span data-ttu-id="56976-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56976-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56976-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56976-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56976-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56976-135">CommonParameters</span></span>
<span data-ttu-id="56976-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56976-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56976-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="56976-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56976-138">輸入</span><span class="sxs-lookup"><span data-stu-id="56976-138">INPUTS</span></span>

### <span data-ttu-id="56976-139">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="56976-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="56976-140">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="56976-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="56976-141">輸出</span><span class="sxs-lookup"><span data-stu-id="56976-141">OUTPUTS</span></span>

### <span data-ttu-id="56976-142">AzureSqlElasticJobCredentialModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="56976-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="56976-143">筆記</span><span class="sxs-lookup"><span data-stu-id="56976-143">NOTES</span></span>

## <span data-ttu-id="56976-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="56976-144">RELATED LINKS</span></span>
