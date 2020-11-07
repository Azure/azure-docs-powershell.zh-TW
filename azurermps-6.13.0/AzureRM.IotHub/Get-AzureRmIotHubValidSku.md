---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: d1c52cef6548f8762f972789a1fd9d47e8cc92aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625832"
---
# <span data-ttu-id="49470-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="49470-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="49470-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49470-102">SYNOPSIS</span></span>
<span data-ttu-id="49470-103">取得此 IotHub 可轉至的所有有效 sku。</span><span class="sxs-lookup"><span data-stu-id="49470-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49470-104">句法</span><span class="sxs-lookup"><span data-stu-id="49470-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49470-105">說明</span><span class="sxs-lookup"><span data-stu-id="49470-105">DESCRIPTION</span></span>
<span data-ttu-id="49470-106">取得此 IotHub 可轉至的所有有效 sku。</span><span class="sxs-lookup"><span data-stu-id="49470-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="49470-107">IotHub 無法在免費和付費的 sku 之間轉換，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="49470-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="49470-108">如果您想要達到這個目的，您必須刪除並重新建立 iothub。</span><span class="sxs-lookup"><span data-stu-id="49470-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="49470-109">示例</span><span class="sxs-lookup"><span data-stu-id="49470-109">EXAMPLES</span></span>

### <span data-ttu-id="49470-110">範例1取得有效的 sku</span><span class="sxs-lookup"><span data-stu-id="49470-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="49470-111">取得名為 "myiothub" 的 IotHub 的所有 sku 清單</span><span class="sxs-lookup"><span data-stu-id="49470-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="49470-112">參數</span><span class="sxs-lookup"><span data-stu-id="49470-112">PARAMETERS</span></span>

### <span data-ttu-id="49470-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49470-113">-DefaultProfile</span></span>
<span data-ttu-id="49470-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="49470-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49470-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="49470-115">-Name</span></span>
<span data-ttu-id="49470-116">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="49470-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="49470-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49470-117">-ResourceGroupName</span></span>
<span data-ttu-id="49470-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="49470-118">Resource Group Name</span></span>

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

### <span data-ttu-id="49470-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49470-119">CommonParameters</span></span>
<span data-ttu-id="49470-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49470-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49470-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49470-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49470-122">輸入</span><span class="sxs-lookup"><span data-stu-id="49470-122">INPUTS</span></span>

### <span data-ttu-id="49470-123">System.object</span><span class="sxs-lookup"><span data-stu-id="49470-123">System.String</span></span>

## <span data-ttu-id="49470-124">輸出</span><span class="sxs-lookup"><span data-stu-id="49470-124">OUTPUTS</span></span>

### <span data-ttu-id="49470-125">PSIotHubSkuDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="49470-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="49470-126">筆記</span><span class="sxs-lookup"><span data-stu-id="49470-126">NOTES</span></span>

## <span data-ttu-id="49470-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="49470-127">RELATED LINKS</span></span>
