---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: d955cb51d92d9d0f3c156900d847e903d642e9af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449980"
---
# <span data-ttu-id="c4403-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c4403-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="c4403-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c4403-102">SYNOPSIS</span></span>
<span data-ttu-id="c4403-103">取得資源群組中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="c4403-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4403-104">句法</span><span class="sxs-lookup"><span data-stu-id="c4403-104">SYNTAX</span></span>

### <span data-ttu-id="c4403-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="c4403-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4403-106">擴充</span><span class="sxs-lookup"><span data-stu-id="c4403-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4403-107">說明</span><span class="sxs-lookup"><span data-stu-id="c4403-107">DESCRIPTION</span></span>
<span data-ttu-id="c4403-108">**AzureRmVirtualNetwork** Cmdlet 會取得一或多個虛擬網路 n a 資源群組。</span><span class="sxs-lookup"><span data-stu-id="c4403-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="c4403-109">示例</span><span class="sxs-lookup"><span data-stu-id="c4403-109">EXAMPLES</span></span>

### <span data-ttu-id="c4403-110">1：檢索虛擬網路</span><span class="sxs-lookup"><span data-stu-id="c4403-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="c4403-111">這個命令會在 [資源] 群組 TestResourceGroup 中取得名為 MyVirtualNetwork 的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="c4403-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="c4403-112">參數</span><span class="sxs-lookup"><span data-stu-id="c4403-112">PARAMETERS</span></span>

### <span data-ttu-id="c4403-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c4403-113">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4403-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="c4403-114">-Name</span></span>
<span data-ttu-id="c4403-115">指定此 Cmdlet 所取得之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4403-115">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4403-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4403-116">-ResourceGroupName</span></span>
<span data-ttu-id="c4403-117">指定虛擬網路所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c4403-117">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4403-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4403-118">-DefaultProfile</span></span>
<span data-ttu-id="c4403-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c4403-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4403-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4403-120">CommonParameters</span></span>
<span data-ttu-id="c4403-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c4403-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4403-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c4403-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4403-123">輸入</span><span class="sxs-lookup"><span data-stu-id="c4403-123">INPUTS</span></span>

## <span data-ttu-id="c4403-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c4403-124">OUTPUTS</span></span>

### <span data-ttu-id="c4403-125">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c4403-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c4403-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c4403-126">NOTES</span></span>

## <span data-ttu-id="c4403-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c4403-127">RELATED LINKS</span></span>

[<span data-ttu-id="c4403-128">新-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c4403-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c4403-129">移除-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c4403-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c4403-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c4403-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


