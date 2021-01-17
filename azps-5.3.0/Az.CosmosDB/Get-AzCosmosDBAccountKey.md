---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/get-azcosmosdbaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Get-AzCosmosDBAccountKey.md
ms.openlocfilehash: b9e78e4ff9811f5ff52b64369fd546d5f5a8c474
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446167"
---
# <span data-ttu-id="9b0f2-101">Get-AzCosmosDBAccountKey</span><span class="sxs-lookup"><span data-stu-id="9b0f2-101">Get-AzCosmosDBAccountKey</span></span>

## <span data-ttu-id="9b0f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9b0f2-103">針對指定的 CosmosDB 帳戶取得 {"ConnectionKeys"、"PrimaryReadOnly" 或 "Keys" 等金鑰。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-103">Get Keys{"ConnectionKeys", "PrimaryReadOnly" or "Keys"} for the given CosmosDB Account.</span></span> 

## <span data-ttu-id="9b0f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b0f2-104">SYNTAX</span></span>

### <span data-ttu-id="9b0f2-105">ByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9b0f2-105">ByNameParameterSet (Default)</span></span>
```
Get-AzCosmosDBAccountKey -ResourceGroupName <String> -Name <String> [-Type <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b0f2-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b0f2-106">ByResourceIdParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b0f2-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b0f2-107">ByObjectParameterSet</span></span>
```
Get-AzCosmosDBAccountKey [-Type <String>] -InputObject <PSDatabaseAccountGetResults>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b0f2-108">說明</span><span class="sxs-lookup"><span data-stu-id="9b0f2-108">DESCRIPTION</span></span>
<span data-ttu-id="9b0f2-109">取得連線金鑰的清單。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-109">Get the list of connection keys.</span></span>

## <span data-ttu-id="9b0f2-110">示例</span><span class="sxs-lookup"><span data-stu-id="9b0f2-110">EXAMPLES</span></span>

### <span data-ttu-id="9b0f2-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9b0f2-111">Example 1</span></span>
```powershell
PS C:\>  Get-AzCosmosDBAccountKey -ResourceGroupName rg1 -Name dbname -Type "ReadOnlyKeys"

Name                           Value
----                           -----
PrimaryReadonlyMasterKey       qjw0ISW1WNN0BIVPeaI7Tm3H8uZ1h7ESQjxaUendxHmIUNQowVvcL84fTqeXoC2HFgyu8Zo1mCFEcg0jZJHPjA==
SecondaryReadonlyMasterKey     9YRcTABuOHcKyHAKf0lmCeHsrcXu02aeID1g3wjXjlX8SU4s2WNlEB5htJoy3xqxNDqIyGfnq3dblLbrZDbesg==
```

<span data-ttu-id="9b0f2-112">列出 [CosmosDB 帳戶] 的按鍵。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-112">Lists the keys for CosmosDB Account.</span></span> <span data-ttu-id="9b0f2-113">金鑰類型可以是來自： ConnectionStrings、Keys 和 ReadOnlyKeys 的值。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-113">The Key Type can be value from : ConnectionStrings, Keys and ReadOnlyKeys.</span></span> <span data-ttu-id="9b0f2-114">預設值為 [金鑰]。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-114">Default is Keys.</span></span>

## <span data-ttu-id="9b0f2-115">參數</span><span class="sxs-lookup"><span data-stu-id="9b0f2-115">PARAMETERS</span></span>

### <span data-ttu-id="9b0f2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b0f2-116">-DefaultProfile</span></span>
<span data-ttu-id="9b0f2-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b0f2-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b0f2-118">-InputObject</span></span>
<span data-ttu-id="9b0f2-119">CosmosDB 帳戶物件</span><span class="sxs-lookup"><span data-stu-id="9b0f2-119">CosmosDB Account object</span></span>

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

### <span data-ttu-id="9b0f2-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b0f2-120">-Name</span></span>
<span data-ttu-id="9b0f2-121">Cosmos DB 資料庫帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-121">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="9b0f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b0f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="9b0f2-123">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-123">Name of resource group.</span></span>

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

### <span data-ttu-id="9b0f2-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b0f2-124">-ResourceId</span></span>
<span data-ttu-id="9b0f2-125">資源的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-125">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="9b0f2-126">-類型</span><span class="sxs-lookup"><span data-stu-id="9b0f2-126">-Type</span></span>
<span data-ttu-id="9b0f2-127">從： {ConnectionStrings，Keys，ReadOnlyKeys} 的值。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-127">Value from: {ConnectionStrings, Keys, ReadOnlyKeys}.</span></span>
<span data-ttu-id="9b0f2-128">預設值為 [金鑰]。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-128">Default is Keys.</span></span>

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

### <span data-ttu-id="9b0f2-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b0f2-129">CommonParameters</span></span>
<span data-ttu-id="9b0f2-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b0f2-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9b0f2-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b0f2-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9b0f2-132">INPUTS</span></span>

### <span data-ttu-id="9b0f2-133">所有</span><span class="sxs-lookup"><span data-stu-id="9b0f2-133">None</span></span>

## <span data-ttu-id="9b0f2-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9b0f2-134">OUTPUTS</span></span>

### <span data-ttu-id="9b0f2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="9b0f2-135">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListConnectionStrings</span></span>

### <span data-ttu-id="9b0f2-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span><span class="sxs-lookup"><span data-stu-id="9b0f2-136">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListKeysResult</span></span>

### <span data-ttu-id="9b0f2-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span><span class="sxs-lookup"><span data-stu-id="9b0f2-137">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccountListReadOnlyKeysResult</span></span>

## <span data-ttu-id="9b0f2-138">筆記</span><span class="sxs-lookup"><span data-stu-id="9b0f2-138">NOTES</span></span>

## <span data-ttu-id="9b0f2-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b0f2-139">RELATED LINKS</span></span>
