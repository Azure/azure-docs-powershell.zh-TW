---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: 62e549ef01f77382226eaf83784add7005516230
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917974"
---
# <span data-ttu-id="872ae-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="872ae-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="872ae-102">簡介</span><span class="sxs-lookup"><span data-stu-id="872ae-102">SYNOPSIS</span></span>
<span data-ttu-id="872ae-103">取得或列出已連結至網路虛擬裝置資源 (網站) 。</span><span class="sxs-lookup"><span data-stu-id="872ae-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="872ae-104">語法</span><span class="sxs-lookup"><span data-stu-id="872ae-104">SYNTAX</span></span>

### <span data-ttu-id="872ae-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="872ae-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="872ae-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="872ae-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="872ae-107">描述</span><span class="sxs-lookup"><span data-stu-id="872ae-107">DESCRIPTION</span></span>
<span data-ttu-id="872ae-108">此Get-AzVirtualApplianceSite可獲取或列出連接至一或多個網路虛擬裝置資源的網站。</span><span class="sxs-lookup"><span data-stu-id="872ae-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="872ae-109">例子</span><span class="sxs-lookup"><span data-stu-id="872ae-109">EXAMPLES</span></span>

### <span data-ttu-id="872ae-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="872ae-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="872ae-111">取得虛擬裝置網站資源。</span><span class="sxs-lookup"><span data-stu-id="872ae-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="872ae-112">範例 2</span><span class="sxs-lookup"><span data-stu-id="872ae-112">Example 2</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite

AddressPrefix     : 10.0.2.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite2
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite2
```

<span data-ttu-id="872ae-113">列出網路虛擬裝置中的虛擬裝置網站資源。</span><span class="sxs-lookup"><span data-stu-id="872ae-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="872ae-114">參數</span><span class="sxs-lookup"><span data-stu-id="872ae-114">PARAMETERS</span></span>

### <span data-ttu-id="872ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872ae-115">-DefaultProfile</span></span>
<span data-ttu-id="872ae-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="872ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="872ae-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="872ae-117">-Name</span></span>
<span data-ttu-id="872ae-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="872ae-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872ae-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="872ae-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="872ae-120">附加網站的網路虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="872ae-120">The Network Virtual Appliance that the site is attached.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="872ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="872ae-122">資源組名。</span><span class="sxs-lookup"><span data-stu-id="872ae-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872ae-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="872ae-123">-ResourceId</span></span>
<span data-ttu-id="872ae-124">虛擬裝置網站的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="872ae-124">The resource Id of the Virtual Appliance Site.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="872ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872ae-125">CommonParameters</span></span>
<span data-ttu-id="872ae-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="872ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872ae-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="872ae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872ae-128">輸入</span><span class="sxs-lookup"><span data-stu-id="872ae-128">INPUTS</span></span>

### <span data-ttu-id="872ae-129">System.String</span><span class="sxs-lookup"><span data-stu-id="872ae-129">System.String</span></span>

## <span data-ttu-id="872ae-130">輸出</span><span class="sxs-lookup"><span data-stu-id="872ae-130">OUTPUTS</span></span>

### <span data-ttu-id="872ae-131">Microsoft.Azure.Commands.Network.models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="872ae-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="872ae-132">筆記</span><span class="sxs-lookup"><span data-stu-id="872ae-132">NOTES</span></span>

## <span data-ttu-id="872ae-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="872ae-133">RELATED LINKS</span></span>
