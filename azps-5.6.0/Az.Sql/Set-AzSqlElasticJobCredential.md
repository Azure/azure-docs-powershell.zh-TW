---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 9c0d7348a900690a49ebea96bc90c296c2d8e9a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910578"
---
# <span data-ttu-id="915ab-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="915ab-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="915ab-102">簡介</span><span class="sxs-lookup"><span data-stu-id="915ab-102">SYNOPSIS</span></span>
<span data-ttu-id="915ab-103">更新工作認證</span><span class="sxs-lookup"><span data-stu-id="915ab-103">Updates a job credential</span></span>

## <span data-ttu-id="915ab-104">語法</span><span class="sxs-lookup"><span data-stu-id="915ab-104">SYNTAX</span></span>

### <span data-ttu-id="915ab-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="915ab-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="915ab-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="915ab-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="915ab-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="915ab-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="915ab-108">描述</span><span class="sxs-lookup"><span data-stu-id="915ab-108">DESCRIPTION</span></span>
<span data-ttu-id="915ab-109">Cmdlet Set-AzSqlElasticJobCredential更新工作認證</span><span class="sxs-lookup"><span data-stu-id="915ab-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="915ab-110">例子</span><span class="sxs-lookup"><span data-stu-id="915ab-110">EXAMPLES</span></span>

### <span data-ttu-id="915ab-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="915ab-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="915ab-112">更新工作認證</span><span class="sxs-lookup"><span data-stu-id="915ab-112">Updates a job credential</span></span>

## <span data-ttu-id="915ab-113">參數</span><span class="sxs-lookup"><span data-stu-id="915ab-113">PARAMETERS</span></span>

### <span data-ttu-id="915ab-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="915ab-114">-AgentName</span></span>
<span data-ttu-id="915ab-115">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="915ab-115">The agent name</span></span>

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

### <span data-ttu-id="915ab-116">-認證</span><span class="sxs-lookup"><span data-stu-id="915ab-116">-Credential</span></span>
<span data-ttu-id="915ab-117">認證</span><span class="sxs-lookup"><span data-stu-id="915ab-117">The credential</span></span>

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

### <span data-ttu-id="915ab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="915ab-118">-DefaultProfile</span></span>
<span data-ttu-id="915ab-119">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="915ab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="915ab-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="915ab-120">-InputObject</span></span>
<span data-ttu-id="915ab-121">工作認證物件</span><span class="sxs-lookup"><span data-stu-id="915ab-121">The job credential object</span></span>

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

### <span data-ttu-id="915ab-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="915ab-122">-Name</span></span>
<span data-ttu-id="915ab-123">工作認證名稱</span><span class="sxs-lookup"><span data-stu-id="915ab-123">The job credential name</span></span>

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

### <span data-ttu-id="915ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="915ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="915ab-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="915ab-125">The resource group name</span></span>

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

### <span data-ttu-id="915ab-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="915ab-126">-ResourceId</span></span>
<span data-ttu-id="915ab-127">工作認證資源識別碼</span><span class="sxs-lookup"><span data-stu-id="915ab-127">The job credential resource id</span></span>

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

### <span data-ttu-id="915ab-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="915ab-128">-ServerName</span></span>
<span data-ttu-id="915ab-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="915ab-129">The server name</span></span>

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

### <span data-ttu-id="915ab-130">-確認</span><span class="sxs-lookup"><span data-stu-id="915ab-130">-Confirm</span></span>
<span data-ttu-id="915ab-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="915ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="915ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="915ab-132">-WhatIf</span></span>
<span data-ttu-id="915ab-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="915ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="915ab-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="915ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="915ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="915ab-135">CommonParameters</span></span>
<span data-ttu-id="915ab-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="915ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="915ab-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="915ab-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="915ab-138">輸入</span><span class="sxs-lookup"><span data-stu-id="915ab-138">INPUTS</span></span>

### <span data-ttu-id="915ab-139">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="915ab-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="915ab-140">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="915ab-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="915ab-141">輸出</span><span class="sxs-lookup"><span data-stu-id="915ab-141">OUTPUTS</span></span>

### <span data-ttu-id="915ab-142">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="915ab-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="915ab-143">筆記</span><span class="sxs-lookup"><span data-stu-id="915ab-143">NOTES</span></span>

## <span data-ttu-id="915ab-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="915ab-144">RELATED LINKS</span></span>
