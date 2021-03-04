---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: c143fed64e99dd9f564b4375c4ef20e5b5ad4354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909854"
---
# <span data-ttu-id="edbfa-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="edbfa-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="edbfa-102">簡介</span><span class="sxs-lookup"><span data-stu-id="edbfa-102">SYNOPSIS</span></span>
<span data-ttu-id="edbfa-103">取得系統管理帳戶的 Keys{"ConnectionKeys"、"PrimaryReadOnly" 或 "Keys"}。</span><span class="sxs-lookup"><span data-stu-id="edbfa-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="edbfa-104">語法</span><span class="sxs-lookup"><span data-stu-id="edbfa-104">SYNTAX</span></span>

### <span data-ttu-id="edbfa-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="edbfa-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edbfa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="edbfa-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="edbfa-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="edbfa-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edbfa-108">描述</span><span class="sxs-lookup"><span data-stu-id="edbfa-108">DESCRIPTION</span></span>
<span data-ttu-id="edbfa-109">取得連接鍵清單。</span><span class="sxs-lookup"><span data-stu-id="edbfa-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="edbfa-110">例子</span><span class="sxs-lookup"><span data-stu-id="edbfa-110">EXAMPLES</span></span>

### <span data-ttu-id="edbfa-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="edbfa-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="edbfa-112">列出管理中心帳戶的金鑰。</span><span class="sxs-lookup"><span data-stu-id="edbfa-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="edbfa-113">Key Type 可以是值：ConnectionStrings、Key 和 ReadOnlyKeys。</span><span class="sxs-lookup"><span data-stu-id="edbfa-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="edbfa-114">預設值為按鍵。</span><span class="sxs-lookup"><span data-stu-id="edbfa-114">Default is Keys.</span></span>

## <span data-ttu-id="edbfa-115">參數</span><span class="sxs-lookup"><span data-stu-id="edbfa-115">PARAMETERS</span></span>

### <span data-ttu-id="edbfa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edbfa-116">-DefaultProfile</span></span>
<span data-ttu-id="edbfa-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="edbfa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbfa-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="edbfa-118">-InputObject</span></span>
<span data-ttu-id="edbfa-119">因此，系統管理資料庫帳戶物件</span><span class="sxs-lookup"><span data-stu-id="edbfa-119">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edbfa-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="edbfa-120">-Name</span></span>
<span data-ttu-id="edbfa-121">系統 DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="edbfa-121">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbfa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edbfa-122">-ResourceGroupName</span></span>
<span data-ttu-id="edbfa-123">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="edbfa-123">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbfa-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="edbfa-124">-ResourceId</span></span>
<span data-ttu-id="edbfa-125">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="edbfa-125">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbfa-126">-類型</span><span class="sxs-lookup"><span data-stu-id="edbfa-126">-Type</span></span>
<span data-ttu-id="edbfa-127">來自：{ConnectionStrings、Keys、ReadOnlyKeys}。</span><span class="sxs-lookup"><span data-stu-id="edbfa-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="edbfa-128">預設值為按鍵。</span><span class="sxs-lookup"><span data-stu-id="edbfa-128">Default is Keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edbfa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edbfa-129">CommonParameters</span></span>
<span data-ttu-id="edbfa-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="edbfa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edbfa-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edbfa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edbfa-132">輸入</span><span class="sxs-lookup"><span data-stu-id="edbfa-132">INPUTS</span></span>

### <span data-ttu-id="edbfa-133">沒有</span><span class="sxs-lookup"><span data-stu-id="edbfa-133">None</span></span>

## <span data-ttu-id="edbfa-134">輸出</span><span class="sxs-lookup"><span data-stu-id="edbfa-134">OUTPUTS</span></span>

### <span data-ttu-id="edbfa-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="edbfa-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="edbfa-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="edbfa-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="edbfa-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="edbfa-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="edbfa-138">筆記</span><span class="sxs-lookup"><span data-stu-id="edbfa-138">NOTES</span></span>

## <span data-ttu-id="edbfa-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="edbfa-139">RELATED LINKS</span></span>
