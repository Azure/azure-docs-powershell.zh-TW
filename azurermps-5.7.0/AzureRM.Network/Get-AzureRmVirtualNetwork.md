---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1745e3a87d91917e762c9b0e441110b4b6945601
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447051"
---
# <span data-ttu-id="6ec59-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ec59-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="6ec59-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6ec59-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec59-103">取得資源群組中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="6ec59-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ec59-104">句法</span><span class="sxs-lookup"><span data-stu-id="6ec59-104">SYNTAX</span></span>

### <span data-ttu-id="6ec59-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="6ec59-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ec59-106">擴充</span><span class="sxs-lookup"><span data-stu-id="6ec59-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ec59-107">說明</span><span class="sxs-lookup"><span data-stu-id="6ec59-107">DESCRIPTION</span></span>
<span data-ttu-id="6ec59-108">**AzureRmVirtualNetwork** Cmdlet 會取得一或多個虛擬網路 n a 資源群組。</span><span class="sxs-lookup"><span data-stu-id="6ec59-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="6ec59-109">示例</span><span class="sxs-lookup"><span data-stu-id="6ec59-109">EXAMPLES</span></span>

### <span data-ttu-id="6ec59-110">1：檢索虛擬網路</span><span class="sxs-lookup"><span data-stu-id="6ec59-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="6ec59-111">這個命令會在 [資源] 群組 TestResourceGroup 中取得名為 MyVirtualNetwork 的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="6ec59-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="6ec59-112">參數</span><span class="sxs-lookup"><span data-stu-id="6ec59-112">PARAMETERS</span></span>

### <span data-ttu-id="6ec59-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec59-113">-DefaultProfile</span></span>
<span data-ttu-id="6ec59-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6ec59-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec59-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="6ec59-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec59-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="6ec59-116">-Name</span></span>
<span data-ttu-id="6ec59-117">指定此 Cmdlet 所取得之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ec59-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec59-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ec59-118">-ResourceGroupName</span></span>
<span data-ttu-id="6ec59-119">指定虛擬網路所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ec59-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec59-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec59-120">CommonParameters</span></span>
<span data-ttu-id="6ec59-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6ec59-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec59-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6ec59-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec59-123">輸入</span><span class="sxs-lookup"><span data-stu-id="6ec59-123">INPUTS</span></span>

### <span data-ttu-id="6ec59-124">所有</span><span class="sxs-lookup"><span data-stu-id="6ec59-124">None</span></span>
<span data-ttu-id="6ec59-125">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6ec59-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ec59-126">輸出</span><span class="sxs-lookup"><span data-stu-id="6ec59-126">OUTPUTS</span></span>

### <span data-ttu-id="6ec59-127">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="6ec59-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="6ec59-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6ec59-128">NOTES</span></span>

## <span data-ttu-id="6ec59-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6ec59-129">RELATED LINKS</span></span>

[<span data-ttu-id="6ec59-130">新-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ec59-130">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6ec59-131">移除-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ec59-131">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="6ec59-132">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ec59-132">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


