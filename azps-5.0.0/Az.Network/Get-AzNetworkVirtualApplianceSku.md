---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkvirtualappliancesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkVirtualApplianceSku.md
ms.openlocfilehash: e38e489207267faf53bb790aaab65ad60c74c8b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137426"
---
# <span data-ttu-id="df149-101">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="df149-101">Get-AzNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="df149-102">摘要</span><span class="sxs-lookup"><span data-stu-id="df149-102">SYNOPSIS</span></span>
<span data-ttu-id="df149-103">在庫存中取得或列出可用的網路虛擬裝置 Sku。</span><span class="sxs-lookup"><span data-stu-id="df149-103">Get or List available Network Virtual Appliance Skus in the inventory.</span></span>

## <span data-ttu-id="df149-104">句法</span><span class="sxs-lookup"><span data-stu-id="df149-104">SYNTAX</span></span>

```
Get-AzNetworkVirtualApplianceSku [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df149-105">說明</span><span class="sxs-lookup"><span data-stu-id="df149-105">DESCRIPTION</span></span>
<span data-ttu-id="df149-106">Get-AzNetworkVirtualApplianceSku 取得或列出 Microsoft Azure 清點中可用的網路虛擬裝置 Sku。</span><span class="sxs-lookup"><span data-stu-id="df149-106">The Get-AzNetworkVirtualApplianceSku gets or lists available Network Virtual Appliance Skus in the Microsoft Azure inventory.</span></span>

## <span data-ttu-id="df149-107">示例</span><span class="sxs-lookup"><span data-stu-id="df149-107">EXAMPLES</span></span>

### <span data-ttu-id="df149-108">範例1</span><span class="sxs-lookup"><span data-stu-id="df149-108">Example 1</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku -SkuName barracudasdwanrelease                                                                                                                        

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="df149-109">依名稱取得 sku。</span><span class="sxs-lookup"><span data-stu-id="df149-109">Get a sku by name.</span></span>

### <span data-ttu-id="df149-110">範例2</span><span class="sxs-lookup"><span data-stu-id="df149-110">Example 2</span></span>
```powershell
PS C:\> Get-AzNetworkVirtualApplianceSku                                                                                                                                                       

Vendor              : barracuda sdwan nightly
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan nightly
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracuda sdwan
AvailableVersions   : {latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracuda sdwan
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :

Vendor              : barracudasdwanrelease
AvailableVersions   : {8.1.0038301, latest}
AvailableScaleUnits : {Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances, Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSkuInstances}
Name                : barracudasdwanrelease
Etag                : 00000000-0000-0000-0000-000000000000
Id                  :
```

<span data-ttu-id="df149-111">列出所有可用的網路虛擬裝置 Sku。</span><span class="sxs-lookup"><span data-stu-id="df149-111">List all available Skus of Network Virtual Appliance.</span></span>

## <span data-ttu-id="df149-112">參數</span><span class="sxs-lookup"><span data-stu-id="df149-112">PARAMETERS</span></span>

### <span data-ttu-id="df149-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df149-113">-DefaultProfile</span></span>
<span data-ttu-id="df149-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="df149-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df149-115">-SkuName</span><span class="sxs-lookup"><span data-stu-id="df149-115">-SkuName</span></span>
<span data-ttu-id="df149-116">Sku 名稱。</span><span class="sxs-lookup"><span data-stu-id="df149-116">The Sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df149-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df149-117">CommonParameters</span></span>
<span data-ttu-id="df149-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="df149-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df149-119">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="df149-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df149-120">輸入</span><span class="sxs-lookup"><span data-stu-id="df149-120">INPUTS</span></span>

### <span data-ttu-id="df149-121">所有</span><span class="sxs-lookup"><span data-stu-id="df149-121">None</span></span>

## <span data-ttu-id="df149-122">輸出</span><span class="sxs-lookup"><span data-stu-id="df149-122">OUTPUTS</span></span>

### <span data-ttu-id="df149-123">PSNetworkVirtualApplianceSku 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="df149-123">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualApplianceSku</span></span>

## <span data-ttu-id="df149-124">筆記</span><span class="sxs-lookup"><span data-stu-id="df149-124">NOTES</span></span>

## <span data-ttu-id="df149-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="df149-125">RELATED LINKS</span></span>
