---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 97ae2607484828350be67cff9c9311fc73f19b6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794363"
---
# <span data-ttu-id="62e7d-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="62e7d-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="62e7d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="62e7d-102">SYNOPSIS</span></span>
<span data-ttu-id="62e7d-103">取得資源群組中的虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="62e7d-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="62e7d-104">句法</span><span class="sxs-lookup"><span data-stu-id="62e7d-104">SYNTAX</span></span>

### <span data-ttu-id="62e7d-105">NoExpand</span><span class="sxs-lookup"><span data-stu-id="62e7d-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62e7d-106">擴充</span><span class="sxs-lookup"><span data-stu-id="62e7d-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62e7d-107">說明</span><span class="sxs-lookup"><span data-stu-id="62e7d-107">DESCRIPTION</span></span>
<span data-ttu-id="62e7d-108">**AzVirtualNetwork** Cmdlet 會取得一或多個虛擬網路 n a 資源群組。</span><span class="sxs-lookup"><span data-stu-id="62e7d-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="62e7d-109">示例</span><span class="sxs-lookup"><span data-stu-id="62e7d-109">EXAMPLES</span></span>

### <span data-ttu-id="62e7d-110">1：檢索虛擬網路</span><span class="sxs-lookup"><span data-stu-id="62e7d-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="62e7d-111">這個命令會在 [資源] 群組 TestResourceGroup 中取得名為 MyVirtualNetwork 的虛擬網路</span><span class="sxs-lookup"><span data-stu-id="62e7d-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="62e7d-112">參數</span><span class="sxs-lookup"><span data-stu-id="62e7d-112">PARAMETERS</span></span>

### <span data-ttu-id="62e7d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62e7d-113">-DefaultProfile</span></span>
<span data-ttu-id="62e7d-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="62e7d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62e7d-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="62e7d-115">-ExpandResource</span></span>
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

### <span data-ttu-id="62e7d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="62e7d-116">-Name</span></span>
<span data-ttu-id="62e7d-117">指定此 Cmdlet 所取得之虛擬網路的名稱。</span><span class="sxs-lookup"><span data-stu-id="62e7d-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="62e7d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62e7d-118">-ResourceGroupName</span></span>
<span data-ttu-id="62e7d-119">指定虛擬網路所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="62e7d-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="62e7d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62e7d-120">CommonParameters</span></span>
<span data-ttu-id="62e7d-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="62e7d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62e7d-122">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="62e7d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62e7d-123">輸入</span><span class="sxs-lookup"><span data-stu-id="62e7d-123">INPUTS</span></span>

## <span data-ttu-id="62e7d-124">輸出</span><span class="sxs-lookup"><span data-stu-id="62e7d-124">OUTPUTS</span></span>

### <span data-ttu-id="62e7d-125">PSVirtualNetwork 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="62e7d-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="62e7d-126">筆記</span><span class="sxs-lookup"><span data-stu-id="62e7d-126">NOTES</span></span>

## <span data-ttu-id="62e7d-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="62e7d-127">RELATED LINKS</span></span>

[<span data-ttu-id="62e7d-128">新-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="62e7d-128">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="62e7d-129">移除-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="62e7d-129">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="62e7d-130">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="62e7d-130">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


