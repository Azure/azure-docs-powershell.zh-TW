---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWan.md
ms.openlocfilehash: d4d9af3184b1b6f858ea4f1e6910fc6562e68f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448375"
---
# <span data-ttu-id="089e4-101">Get-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="089e4-101">Get-AzureRmVirtualWan</span></span>

## <span data-ttu-id="089e4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="089e4-102">SYNOPSIS</span></span>
<span data-ttu-id="089e4-103">取得資源群組或訂閱中的虛擬 WAN 或所有虛擬 Wan。</span><span class="sxs-lookup"><span data-stu-id="089e4-103">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="089e4-104">句法</span><span class="sxs-lookup"><span data-stu-id="089e4-104">SYNTAX</span></span>

### <span data-ttu-id="089e4-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="089e4-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualWan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="089e4-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="089e4-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualWan -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="089e4-107">說明</span><span class="sxs-lookup"><span data-stu-id="089e4-107">DESCRIPTION</span></span>
<span data-ttu-id="089e4-108">取得資源群組或訂閱中的虛擬 WAN 或所有虛擬 Wan。</span><span class="sxs-lookup"><span data-stu-id="089e4-108">Gets a Virtual WAN or all Virtual WANs in a resource group or subscription.</span></span>

## <span data-ttu-id="089e4-109">示例</span><span class="sxs-lookup"><span data-stu-id="089e4-109">EXAMPLES</span></span>

### <span data-ttu-id="089e4-110">範例1</span><span class="sxs-lookup"><span data-stu-id="089e4-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true
PS C:\> Get-AzureRmVirtualWan -Name "myVirtualWAN" -ResourceGroupName "testRG"

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="089e4-111">這個命令會取得資源群組 testRG 中名為 myVirtualWAN 的虛擬 WAN。</span><span class="sxs-lookup"><span data-stu-id="089e4-111">This command gets the Virtual WAN named myVirtualWAN in the resource group testRG.</span></span>

## <span data-ttu-id="089e4-112">參數</span><span class="sxs-lookup"><span data-stu-id="089e4-112">PARAMETERS</span></span>

### <span data-ttu-id="089e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="089e4-113">-DefaultProfile</span></span>
<span data-ttu-id="089e4-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="089e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="089e4-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="089e4-115">-Name</span></span>
<span data-ttu-id="089e4-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="089e4-116">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089e4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="089e4-117">-ResourceGroupName</span></span>
<span data-ttu-id="089e4-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="089e4-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="089e4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="089e4-119">CommonParameters</span></span>
<span data-ttu-id="089e4-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="089e4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="089e4-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="089e4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="089e4-122">輸入</span><span class="sxs-lookup"><span data-stu-id="089e4-122">INPUTS</span></span>

### <span data-ttu-id="089e4-123">所有</span><span class="sxs-lookup"><span data-stu-id="089e4-123">None</span></span>

## <span data-ttu-id="089e4-124">輸出</span><span class="sxs-lookup"><span data-stu-id="089e4-124">OUTPUTS</span></span>

### <span data-ttu-id="089e4-125">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="089e4-125">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="089e4-126">筆記</span><span class="sxs-lookup"><span data-stu-id="089e4-126">NOTES</span></span>

## <span data-ttu-id="089e4-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="089e4-127">RELATED LINKS</span></span>
