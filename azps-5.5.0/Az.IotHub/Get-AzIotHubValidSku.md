---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133115"
---
# <span data-ttu-id="bd508-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="bd508-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="bd508-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd508-102">SYNOPSIS</span></span>
<span data-ttu-id="bd508-103">取得此 IotHub 可轉至的所有有效 sku。</span><span class="sxs-lookup"><span data-stu-id="bd508-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="bd508-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd508-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd508-105">說明</span><span class="sxs-lookup"><span data-stu-id="bd508-105">DESCRIPTION</span></span>
<span data-ttu-id="bd508-106">取得此 IotHub 可轉至的所有有效 sku。</span><span class="sxs-lookup"><span data-stu-id="bd508-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="bd508-107">IotHub 無法在免費和付費的 sku 之間轉換，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="bd508-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="bd508-108">如果您想要達到這個目的，您必須刪除並重新建立 iothub。</span><span class="sxs-lookup"><span data-stu-id="bd508-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="bd508-109">示例</span><span class="sxs-lookup"><span data-stu-id="bd508-109">EXAMPLES</span></span>

### <span data-ttu-id="bd508-110">範例1取得有效的 sku</span><span class="sxs-lookup"><span data-stu-id="bd508-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="bd508-111">取得名為 "myiothub" 的 IotHub 的所有 sku 清單</span><span class="sxs-lookup"><span data-stu-id="bd508-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="bd508-112">參數</span><span class="sxs-lookup"><span data-stu-id="bd508-112">PARAMETERS</span></span>

### <span data-ttu-id="bd508-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd508-113">-DefaultProfile</span></span>
<span data-ttu-id="bd508-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bd508-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd508-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd508-115">-Name</span></span>
<span data-ttu-id="bd508-116">IoT 中樞的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd508-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="bd508-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd508-117">-ResourceGroupName</span></span>
<span data-ttu-id="bd508-118">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="bd508-118">Resource Group Name</span></span>

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

### <span data-ttu-id="bd508-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd508-119">CommonParameters</span></span>
<span data-ttu-id="bd508-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd508-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd508-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bd508-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd508-122">輸入</span><span class="sxs-lookup"><span data-stu-id="bd508-122">INPUTS</span></span>

### <span data-ttu-id="bd508-123">System.object</span><span class="sxs-lookup"><span data-stu-id="bd508-123">System.String</span></span>

## <span data-ttu-id="bd508-124">輸出</span><span class="sxs-lookup"><span data-stu-id="bd508-124">OUTPUTS</span></span>

### <span data-ttu-id="bd508-125">PSIotHubSkuDescription （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="bd508-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="bd508-126">筆記</span><span class="sxs-lookup"><span data-stu-id="bd508-126">NOTES</span></span>

## <span data-ttu-id="bd508-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd508-127">RELATED LINKS</span></span>
