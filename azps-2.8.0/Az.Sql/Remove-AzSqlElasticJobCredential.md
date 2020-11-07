---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1986a773a61f9c0ac1bd9a30992db3843b97e438
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792423"
---
# <span data-ttu-id="9641b-101">Remove-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="9641b-101">Remove-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="9641b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9641b-102">SYNOPSIS</span></span>
<span data-ttu-id="9641b-103">移除彈性作業認證</span><span class="sxs-lookup"><span data-stu-id="9641b-103">Removes the elastic job credential</span></span>

## <span data-ttu-id="9641b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9641b-104">SYNTAX</span></span>

### <span data-ttu-id="9641b-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9641b-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9641b-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="9641b-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9641b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9641b-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobCredential [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9641b-108">說明</span><span class="sxs-lookup"><span data-stu-id="9641b-108">DESCRIPTION</span></span>
<span data-ttu-id="9641b-109">Remove-AzSqlElasticJobCredential Cmdlet 會移除作業認證</span><span class="sxs-lookup"><span data-stu-id="9641b-109">The Remove-AzSqlElasticJobCredential cmdlet removes a job credential</span></span>

## <span data-ttu-id="9641b-110">示例</span><span class="sxs-lookup"><span data-stu-id="9641b-110">EXAMPLES</span></span>

### <span data-ttu-id="9641b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9641b-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Remove-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="9641b-112">移除作業認證</span><span class="sxs-lookup"><span data-stu-id="9641b-112">Removes a job credential</span></span>

## <span data-ttu-id="9641b-113">參數</span><span class="sxs-lookup"><span data-stu-id="9641b-113">PARAMETERS</span></span>

### <span data-ttu-id="9641b-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9641b-114">-AgentName</span></span>
<span data-ttu-id="9641b-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="9641b-115">The agent name</span></span>

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

### <span data-ttu-id="9641b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9641b-116">-DefaultProfile</span></span>
<span data-ttu-id="9641b-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9641b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9641b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9641b-118">-InputObject</span></span>
<span data-ttu-id="9641b-119">作業憑證物件</span><span class="sxs-lookup"><span data-stu-id="9641b-119">The job credential object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9641b-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9641b-120">-Name</span></span>
<span data-ttu-id="9641b-121">作業認證名稱</span><span class="sxs-lookup"><span data-stu-id="9641b-121">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: CredentialName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9641b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9641b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9641b-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="9641b-123">The resource group name</span></span>

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

### <span data-ttu-id="9641b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9641b-124">-ResourceId</span></span>
<span data-ttu-id="9641b-125">作業身分識別資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9641b-125">The job credential resource id</span></span>

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

### <span data-ttu-id="9641b-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9641b-126">-ServerName</span></span>
<span data-ttu-id="9641b-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="9641b-127">The server name</span></span>

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

### <span data-ttu-id="9641b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="9641b-128">-Confirm</span></span>
<span data-ttu-id="9641b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9641b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9641b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9641b-130">-WhatIf</span></span>
<span data-ttu-id="9641b-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9641b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9641b-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9641b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9641b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9641b-133">CommonParameters</span></span>
<span data-ttu-id="9641b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9641b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9641b-135">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9641b-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9641b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="9641b-136">INPUTS</span></span>

### <span data-ttu-id="9641b-137">AzureSqlElasticJobCredentialModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="9641b-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="9641b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="9641b-138">OUTPUTS</span></span>

### <span data-ttu-id="9641b-139">AzureSqlElasticJobCredentialModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="9641b-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="9641b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="9641b-140">NOTES</span></span>

## <span data-ttu-id="9641b-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="9641b-141">RELATED LINKS</span></span>
