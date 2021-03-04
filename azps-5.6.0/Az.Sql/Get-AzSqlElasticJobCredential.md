---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 466df2e5be2c9193cce49cf9b06a5f8ff0d10e94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917566"
---
# <span data-ttu-id="a9f02-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="a9f02-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="a9f02-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a9f02-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f02-103">獲得一或多個認證</span><span class="sxs-lookup"><span data-stu-id="a9f02-103">Gets one or more credentials</span></span>

## <span data-ttu-id="a9f02-104">語法</span><span class="sxs-lookup"><span data-stu-id="a9f02-104">SYNTAX</span></span>

### <span data-ttu-id="a9f02-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a9f02-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9f02-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9f02-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9f02-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9f02-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9f02-108">描述</span><span class="sxs-lookup"><span data-stu-id="a9f02-108">DESCRIPTION</span></span>
<span data-ttu-id="a9f02-109">Cmdlet Get-AzSqlElasticJobCredential一或多個工作認證</span><span class="sxs-lookup"><span data-stu-id="a9f02-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="a9f02-110">例子</span><span class="sxs-lookup"><span data-stu-id="a9f02-110">EXAMPLES</span></span>

### <span data-ttu-id="a9f02-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="a9f02-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="a9f02-112">獲得工作認證</span><span class="sxs-lookup"><span data-stu-id="a9f02-112">Gets a job credential</span></span>

## <span data-ttu-id="a9f02-113">參數</span><span class="sxs-lookup"><span data-stu-id="a9f02-113">PARAMETERS</span></span>

### <span data-ttu-id="a9f02-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="a9f02-114">-AgentName</span></span>
<span data-ttu-id="a9f02-115">代理人名稱</span><span class="sxs-lookup"><span data-stu-id="a9f02-115">The agent name</span></span>

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

### <span data-ttu-id="a9f02-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f02-116">-DefaultProfile</span></span>
<span data-ttu-id="a9f02-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="a9f02-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9f02-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9f02-118">-Name</span></span>
<span data-ttu-id="a9f02-119">工作認證名稱</span><span class="sxs-lookup"><span data-stu-id="a9f02-119">The job credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CredentialName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9f02-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a9f02-120">-ParentObject</span></span>
<span data-ttu-id="a9f02-121">代理程式物件</span><span class="sxs-lookup"><span data-stu-id="a9f02-121">The agent object</span></span>

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

### <span data-ttu-id="a9f02-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a9f02-122">-ParentResourceId</span></span>
<span data-ttu-id="a9f02-123">代理程式資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a9f02-123">The agent resource id</span></span>

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

### <span data-ttu-id="a9f02-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9f02-124">-ResourceGroupName</span></span>
<span data-ttu-id="a9f02-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="a9f02-125">The resource group name</span></span>

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

### <span data-ttu-id="a9f02-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a9f02-126">-ServerName</span></span>
<span data-ttu-id="a9f02-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="a9f02-127">The server name</span></span>

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

### <span data-ttu-id="a9f02-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f02-128">CommonParameters</span></span>
<span data-ttu-id="a9f02-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a9f02-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f02-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a9f02-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f02-131">輸入</span><span class="sxs-lookup"><span data-stu-id="a9f02-131">INPUTS</span></span>

### <span data-ttu-id="a9f02-132">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="a9f02-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="a9f02-133">輸出</span><span class="sxs-lookup"><span data-stu-id="a9f02-133">OUTPUTS</span></span>

### <span data-ttu-id="a9f02-134">Microsoft.Azure.Commands.Sql.AzureJobs.Model.AzureSqlElasticJobCredentialModel</span><span class="sxs-lookup"><span data-stu-id="a9f02-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="a9f02-135">筆記</span><span class="sxs-lookup"><span data-stu-id="a9f02-135">NOTES</span></span>

## <span data-ttu-id="a9f02-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9f02-136">RELATED LINKS</span></span>
