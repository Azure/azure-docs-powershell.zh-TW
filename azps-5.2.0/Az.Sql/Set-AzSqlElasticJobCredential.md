---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: 87ac0ddaa205c2b257a3aadf9ceea5a6ec302eab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284648"
---
# <span data-ttu-id="c757a-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="c757a-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="c757a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c757a-102">SYNOPSIS</span></span>
<span data-ttu-id="c757a-103">更新作業認證</span><span class="sxs-lookup"><span data-stu-id="c757a-103">Updates a job credential</span></span>

## <span data-ttu-id="c757a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c757a-104">SYNTAX</span></span>

### <span data-ttu-id="c757a-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="c757a-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c757a-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c757a-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c757a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c757a-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c757a-108">說明</span><span class="sxs-lookup"><span data-stu-id="c757a-108">DESCRIPTION</span></span>
<span data-ttu-id="c757a-109">Set-AzSqlElasticJobCredential Cmdlet 會更新作業認證</span><span class="sxs-lookup"><span data-stu-id="c757a-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="c757a-110">示例</span><span class="sxs-lookup"><span data-stu-id="c757a-110">EXAMPLES</span></span>

### <span data-ttu-id="c757a-111">範例1</span><span class="sxs-lookup"><span data-stu-id="c757a-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="c757a-112">更新作業認證</span><span class="sxs-lookup"><span data-stu-id="c757a-112">Updates a job credential</span></span>

## <span data-ttu-id="c757a-113">參數</span><span class="sxs-lookup"><span data-stu-id="c757a-113">PARAMETERS</span></span>

### <span data-ttu-id="c757a-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c757a-114">-AgentName</span></span>
<span data-ttu-id="c757a-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="c757a-115">The agent name</span></span>

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

### <span data-ttu-id="c757a-116">-認證</span><span class="sxs-lookup"><span data-stu-id="c757a-116">-Credential</span></span>
<span data-ttu-id="c757a-117">認證</span><span class="sxs-lookup"><span data-stu-id="c757a-117">The credential</span></span>

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

### <span data-ttu-id="c757a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c757a-118">-DefaultProfile</span></span>
<span data-ttu-id="c757a-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c757a-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c757a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c757a-120">-InputObject</span></span>
<span data-ttu-id="c757a-121">作業憑證物件</span><span class="sxs-lookup"><span data-stu-id="c757a-121">The job credential object</span></span>

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

### <span data-ttu-id="c757a-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="c757a-122">-Name</span></span>
<span data-ttu-id="c757a-123">作業認證名稱</span><span class="sxs-lookup"><span data-stu-id="c757a-123">The job credential name</span></span>

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

### <span data-ttu-id="c757a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c757a-124">-ResourceGroupName</span></span>
<span data-ttu-id="c757a-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="c757a-125">The resource group name</span></span>

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

### <span data-ttu-id="c757a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c757a-126">-ResourceId</span></span>
<span data-ttu-id="c757a-127">作業身分識別資源識別碼</span><span class="sxs-lookup"><span data-stu-id="c757a-127">The job credential resource id</span></span>

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

### <span data-ttu-id="c757a-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c757a-128">-ServerName</span></span>
<span data-ttu-id="c757a-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="c757a-129">The server name</span></span>

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

### <span data-ttu-id="c757a-130">-確認</span><span class="sxs-lookup"><span data-stu-id="c757a-130">-Confirm</span></span>
<span data-ttu-id="c757a-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c757a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c757a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c757a-132">-WhatIf</span></span>
<span data-ttu-id="c757a-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c757a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c757a-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c757a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c757a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c757a-135">CommonParameters</span></span>
<span data-ttu-id="c757a-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c757a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c757a-137">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c757a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c757a-138">輸入</span><span class="sxs-lookup"><span data-stu-id="c757a-138">INPUTS</span></span>

### <span data-ttu-id="c757a-139">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="c757a-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="c757a-140">AzureSqlElasticJobCredentialModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="c757a-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="c757a-141">輸出</span><span class="sxs-lookup"><span data-stu-id="c757a-141">OUTPUTS</span></span>

### <span data-ttu-id="c757a-142">AzureSqlElasticJobCredentialModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="c757a-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="c757a-143">筆記</span><span class="sxs-lookup"><span data-stu-id="c757a-143">NOTES</span></span>

## <span data-ttu-id="c757a-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="c757a-144">RELATED LINKS</span></span>
