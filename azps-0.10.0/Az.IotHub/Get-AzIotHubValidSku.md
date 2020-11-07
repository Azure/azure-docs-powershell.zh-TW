---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: f2d7c10e29209870d4aa6e5176731b07f7695aff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795610"
---
# <span data-ttu-id="535c1-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="535c1-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="535c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="535c1-102">SYNOPSIS</span></span>
<span data-ttu-id="535c1-103">取得此 IotHub 可轉至的所有有效 sku。</span><span class="sxs-lookup"><span data-stu-id="535c1-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="535c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="535c1-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="535c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="535c1-105">DESCRIPTION</span></span>
<span data-ttu-id="535c1-106">取得此 IotHub 可轉至的所有有效 sku。</span><span class="sxs-lookup"><span data-stu-id="535c1-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="535c1-107">IotHub 無法在免費和付費的 sku 之間轉換，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="535c1-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="535c1-108">如果您想要達到這個目的，您必須刪除並重新建立 iothub。</span><span class="sxs-lookup"><span data-stu-id="535c1-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="535c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="535c1-109">EXAMPLES</span></span>

### <span data-ttu-id="535c1-110">範例1取得有效的 sku</span><span class="sxs-lookup"><span data-stu-id="535c1-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="535c1-111">取得名為 "myiothub" 的 IotHub 的所有 sku 清單</span><span class="sxs-lookup"><span data-stu-id="535c1-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="535c1-112">參數</span><span class="sxs-lookup"><span data-stu-id="535c1-112">PARAMETERS</span></span>

### <span data-ttu-id="535c1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535c1-113">-DefaultProfile</span></span>
<span data-ttu-id="535c1-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="535c1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="535c1-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="535c1-115">-Name</span></span>
<span data-ttu-id="535c1-116">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="535c1-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="535c1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="535c1-117">-ResourceGroupName</span></span>
<span data-ttu-id="535c1-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="535c1-118">Resource Group Name</span></span>

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

### <span data-ttu-id="535c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535c1-119">CommonParameters</span></span>
<span data-ttu-id="535c1-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="535c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535c1-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="535c1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535c1-122">輸入</span><span class="sxs-lookup"><span data-stu-id="535c1-122">INPUTS</span></span>

### <span data-ttu-id="535c1-123">System.object</span><span class="sxs-lookup"><span data-stu-id="535c1-123">System.String</span></span>

## <span data-ttu-id="535c1-124">輸出</span><span class="sxs-lookup"><span data-stu-id="535c1-124">OUTPUTS</span></span>

### <span data-ttu-id="535c1-125">PSIotHubSkuDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="535c1-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="535c1-126">筆記</span><span class="sxs-lookup"><span data-stu-id="535c1-126">NOTES</span></span>

## <span data-ttu-id="535c1-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="535c1-127">RELATED LINKS</span></span>
