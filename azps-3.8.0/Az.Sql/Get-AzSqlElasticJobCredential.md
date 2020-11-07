---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobCredential.md
ms.openlocfilehash: 1cd466581a89e49280d2a6cacdd74d4d37ac208d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93799094"
---
# <span data-ttu-id="e397f-101">Get-AzSqlElasticJobCredential</span><span class="sxs-lookup"><span data-stu-id="e397f-101">Get-AzSqlElasticJobCredential</span></span>

## <span data-ttu-id="e397f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e397f-102">SYNOPSIS</span></span>
<span data-ttu-id="e397f-103">取得一或多個認證</span><span class="sxs-lookup"><span data-stu-id="e397f-103">Gets one or more credentials</span></span>

## <span data-ttu-id="e397f-104">句法</span><span class="sxs-lookup"><span data-stu-id="e397f-104">SYNTAX</span></span>

### <span data-ttu-id="e397f-105">DefaultSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e397f-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobCredential [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e397f-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="e397f-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e397f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e397f-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobCredential [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e397f-108">說明</span><span class="sxs-lookup"><span data-stu-id="e397f-108">DESCRIPTION</span></span>
<span data-ttu-id="e397f-109">Get-AzSqlElasticJobCredential Cmdlet 會取得一或多個作業認證</span><span class="sxs-lookup"><span data-stu-id="e397f-109">The Get-AzSqlElasticJobCredential cmdlet gets one or more job credentials</span></span>

## <span data-ttu-id="e397f-110">示例</span><span class="sxs-lookup"><span data-stu-id="e397f-110">EXAMPLES</span></span>

### <span data-ttu-id="e397f-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e397f-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobCredential -Name cred1

CredentialName UserName
-------------- --------
cred1          user1
```

<span data-ttu-id="e397f-112">取得作業認證</span><span class="sxs-lookup"><span data-stu-id="e397f-112">Gets a job credential</span></span>

## <span data-ttu-id="e397f-113">參數</span><span class="sxs-lookup"><span data-stu-id="e397f-113">PARAMETERS</span></span>

### <span data-ttu-id="e397f-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e397f-114">-AgentName</span></span>
<span data-ttu-id="e397f-115">代理程式名稱</span><span class="sxs-lookup"><span data-stu-id="e397f-115">The agent name</span></span>

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

### <span data-ttu-id="e397f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e397f-116">-DefaultProfile</span></span>
<span data-ttu-id="e397f-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e397f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e397f-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e397f-118">-Name</span></span>
<span data-ttu-id="e397f-119">作業認證名稱</span><span class="sxs-lookup"><span data-stu-id="e397f-119">The job credential name</span></span>

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

### <span data-ttu-id="e397f-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e397f-120">-ParentObject</span></span>
<span data-ttu-id="e397f-121">Agent 物件</span><span class="sxs-lookup"><span data-stu-id="e397f-121">The agent object</span></span>

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

### <span data-ttu-id="e397f-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e397f-122">-ParentResourceId</span></span>
<span data-ttu-id="e397f-123">Agent 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e397f-123">The agent resource id</span></span>

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

### <span data-ttu-id="e397f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e397f-124">-ResourceGroupName</span></span>
<span data-ttu-id="e397f-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="e397f-125">The resource group name</span></span>

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

### <span data-ttu-id="e397f-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e397f-126">-ServerName</span></span>
<span data-ttu-id="e397f-127">伺服器名稱</span><span class="sxs-lookup"><span data-stu-id="e397f-127">The server name</span></span>

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

### <span data-ttu-id="e397f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e397f-128">CommonParameters</span></span>
<span data-ttu-id="e397f-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e397f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e397f-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e397f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e397f-131">輸入</span><span class="sxs-lookup"><span data-stu-id="e397f-131">INPUTS</span></span>

### <span data-ttu-id="e397f-132">AzureSqlElasticJobAgentModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="e397f-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="e397f-133">輸出</span><span class="sxs-lookup"><span data-stu-id="e397f-133">OUTPUTS</span></span>

### <span data-ttu-id="e397f-134">AzureSqlElasticJobCredentialModel 中的 [ElasticJobs]</span><span class="sxs-lookup"><span data-stu-id="e397f-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobCredentialModel</span></span>

## <span data-ttu-id="e397f-135">筆記</span><span class="sxs-lookup"><span data-stu-id="e397f-135">NOTES</span></span>

## <span data-ttu-id="e397f-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="e397f-136">RELATED LINKS</span></span>
