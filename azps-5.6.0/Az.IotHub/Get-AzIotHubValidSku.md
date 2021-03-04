---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: b51c41ddd36d19afedd0091be9b0a00bb447faaa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905077"
---
# <span data-ttu-id="44ba4-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="44ba4-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="44ba4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="44ba4-102">SYNOPSIS</span></span>
<span data-ttu-id="44ba4-103">會獲得此 IotHub 可以轉換到的所有有效 SKU。</span><span class="sxs-lookup"><span data-stu-id="44ba4-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="44ba4-104">語法</span><span class="sxs-lookup"><span data-stu-id="44ba4-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="44ba4-105">描述</span><span class="sxs-lookup"><span data-stu-id="44ba4-105">DESCRIPTION</span></span>
<span data-ttu-id="44ba4-106">獲得此 IotHub 可以轉換到的所有有效 SKU。</span><span class="sxs-lookup"><span data-stu-id="44ba4-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="44ba4-107">IotHub 無法在免費和付費 SKU 之間轉換，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="44ba4-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="44ba4-108">若要達到此目的，您必須刪除並重新重新使用 iothub。</span><span class="sxs-lookup"><span data-stu-id="44ba4-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="44ba4-109">例子</span><span class="sxs-lookup"><span data-stu-id="44ba4-109">EXAMPLES</span></span>

### <span data-ttu-id="44ba4-110">範例 1 取得有效的 SKU</span><span class="sxs-lookup"><span data-stu-id="44ba4-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="44ba4-111">獲得名稱為"myiothub" 的 IotHub 所有 SKU 清單</span><span class="sxs-lookup"><span data-stu-id="44ba4-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="44ba4-112">參數</span><span class="sxs-lookup"><span data-stu-id="44ba4-112">PARAMETERS</span></span>

### <span data-ttu-id="44ba4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ba4-113">-DefaultProfile</span></span>
<span data-ttu-id="44ba4-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="44ba4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44ba4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="44ba4-115">-Name</span></span>
<span data-ttu-id="44ba4-116">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="44ba4-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44ba4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ba4-117">-ResourceGroupName</span></span>
<span data-ttu-id="44ba4-118">資源組名</span><span class="sxs-lookup"><span data-stu-id="44ba4-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44ba4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ba4-119">CommonParameters</span></span>
<span data-ttu-id="44ba4-120">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="44ba4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ba4-121">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="44ba4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ba4-122">輸入</span><span class="sxs-lookup"><span data-stu-id="44ba4-122">INPUTS</span></span>

### <span data-ttu-id="44ba4-123">System.String</span><span class="sxs-lookup"><span data-stu-id="44ba4-123">System.String</span></span>

## <span data-ttu-id="44ba4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="44ba4-124">OUTPUTS</span></span>

### <span data-ttu-id="44ba4-125">Microsoft.Azure.Commands.management.IotHub.models.PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="44ba4-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="44ba4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="44ba4-126">NOTES</span></span>

## <span data-ttu-id="44ba4-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="44ba4-127">RELATED LINKS</span></span>
