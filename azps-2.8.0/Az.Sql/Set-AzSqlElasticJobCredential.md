---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobCredential.md
ms.openlocfilehash: b3e3aa1414b24324278f4191fd53a28a75d0cfab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93792589"
---
# <span data-ttu-id="4e892-101">Set-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="4e892-101">Set-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="4e892-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e892-102">SYNOPSIS</span></span>
<span data-ttu-id="4e892-103">更新作業認證</span><span class="sxs-lookup"><span data-stu-id="4e892-103">Updates a job credential</span></span>

## <span data-ttu-id="4e892-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e892-104">SYNTAX</span></span>

### <span data-ttu-id="4e892-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4e892-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> -Credential <PSCredential> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e892-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="4e892-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobCredential [-InputObject] <AzureSqlElasticJobCredentialModel> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e892-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4e892-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobCredential [-ResourceId] <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e892-108">說明</span><span class="sxs-lookup"><span data-stu-id="4e892-108">DESCRIPTION</span></span>
<span data-ttu-id="4e892-109">Set-AzSqlElasticJobCredential Cmdlet 會更新作業認證</span><span class="sxs-lookup"><span data-stu-id="4e892-109">The Set-AzSqlElasticJobCredential cmdlet updates a job credential</span></span>

## <span data-ttu-id="4e892-110">示例</span><span class="sxs-lookup"><span data-stu-id="4e892-110">EXAMPLES</span></span>

### <span data-ttu-id="4e892-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4e892-111">Example 1</span></span>
```
PS C:\> $cred = Get-AzSqlElasticJobCredential -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name cred1
$cred | Set-AzSqlElasticJobCredential -Name cred1 -Credential (Get-Credential)

CredentialName UserName
-------------- --------
cred1          user2
```

<span data-ttu-id="4e892-112">更新作業認證</span><span class="sxs-lookup"><span data-stu-id="4e892-112">Updates a job credential</span></span>

## <span data-ttu-id="4e892-113">參數</span><span class="sxs-lookup"><span data-stu-id="4e892-113">PARAMETERS</span></span>

### <span data-ttu-id="4e892-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4e892-114">-AgentName</span></span>
<span data-ttu-id="4e892-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="4e892-115">The agent name</span></span>

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

### <span data-ttu-id="4e892-116">-認證</span><span class="sxs-lookup"><span data-stu-id="4e892-116">-Credential</span></span>
<span data-ttu-id="4e892-117">認證</span><span class="sxs-lookup"><span data-stu-id="4e892-117">The credential</span></span>

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

### <span data-ttu-id="4e892-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e892-118">-DefaultProfile</span></span>
<span data-ttu-id="4e892-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e892-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e892-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e892-120">-InputObject</span></span>
<span data-ttu-id="4e892-121">作業憑證物件</span><span class="sxs-lookup"><span data-stu-id="4e892-121">The job credential object</span></span>

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

### <span data-ttu-id="4e892-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e892-122">-Name</span></span>
<span data-ttu-id="4e892-123">作業認證名稱</span><span class="sxs-lookup"><span data-stu-id="4e892-123">The job credential name</span></span>

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

### <span data-ttu-id="4e892-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e892-124">-ResourceGroupName</span></span>
<span data-ttu-id="4e892-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="4e892-125">The resource group name</span></span>

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

### <span data-ttu-id="4e892-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e892-126">-ResourceId</span></span>
<span data-ttu-id="4e892-127">作業身分識別資源識別碼</span><span class="sxs-lookup"><span data-stu-id="4e892-127">The job credential resource id</span></span>

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

### <span data-ttu-id="4e892-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e892-128">-ServerName</span></span>
<span data-ttu-id="4e892-129">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="4e892-129">The server name</span></span>

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

### <span data-ttu-id="4e892-130">-確認</span><span class="sxs-lookup"><span data-stu-id="4e892-130">-Confirm</span></span>
<span data-ttu-id="4e892-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e892-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e892-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e892-132">-WhatIf</span></span>
<span data-ttu-id="4e892-133">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e892-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e892-134">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e892-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e892-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e892-135">CommonParameters</span></span>
<span data-ttu-id="4e892-136">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e892-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e892-137">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e892-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e892-138">輸入</span><span class="sxs-lookup"><span data-stu-id="4e892-138">INPUTS</span></span>

### <span data-ttu-id="4e892-139">系統管理. PSCredential</span><span class="sxs-lookup"><span data-stu-id="4e892-139">System.Management.Automation.PSCredential</span></span>
### <span data-ttu-id="4e892-140">AzureSqlElasticJobCredentialModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="4e892-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="4e892-141">輸出</span><span class="sxs-lookup"><span data-stu-id="4e892-141">OUTPUTS</span></span>

### <span data-ttu-id="4e892-142">AzureSqlElasticJobCredentialModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="4e892-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="4e892-143">筆記</span><span class="sxs-lookup"><span data-stu-id="4e892-143">NOTES</span></span>

## <span data-ttu-id="4e892-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e892-144">RELATED LINKS</span></span>
