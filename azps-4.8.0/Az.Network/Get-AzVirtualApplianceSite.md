---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualApplianceSite.md
ms.openlocfilehash: b21fe2cc51668548d4fedc8eb6fc9404d5626a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126988"
---
# <span data-ttu-id="4ac26-101">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="4ac26-101">Get-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="4ac26-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4ac26-102">SYNOPSIS</span></span>
<span data-ttu-id="4ac26-103">取得或列出連線至網路虛擬裝置資源 (s 的網站) 。</span><span class="sxs-lookup"><span data-stu-id="4ac26-103">Get or List sites connected to Network Virtual Appliance resource(s).</span></span>

## <span data-ttu-id="4ac26-104">句法</span><span class="sxs-lookup"><span data-stu-id="4ac26-104">SYNTAX</span></span>

### <span data-ttu-id="4ac26-105">ResourceNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4ac26-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzVirtualApplianceSite [-Name <String>] [-NetworkVirtualApplianceId <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ac26-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4ac26-106">ResourceIdParameterSet</span></span>
```
Get-AzVirtualApplianceSite -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ac26-107">說明</span><span class="sxs-lookup"><span data-stu-id="4ac26-107">DESCRIPTION</span></span>
<span data-ttu-id="4ac26-108">Get-AzVirtualApplianceSite 取得或列出連線至一或多個網路虛擬裝置資源的網站。</span><span class="sxs-lookup"><span data-stu-id="4ac26-108">The Get-AzVirtualApplianceSite gets or lists sites connected to one or more Network Virtual Appliance resources.</span></span>

## <span data-ttu-id="4ac26-109">示例</span><span class="sxs-lookup"><span data-stu-id="4ac26-109">EXAMPLES</span></span>

### <span data-ttu-id="4ac26-110">範例1</span><span class="sxs-lookup"><span data-stu-id="4ac26-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualApplianceSite -Name testsite -NetworkVirtualApplianceId $nva.Id -ResourceGroupName testrg


AddressPrefix     : 10.0.1.0/24
O365Policy        : Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties
ProvisioningState : Succeeded
Name              : testsite
Etag              : 00000000-0000-0000-0000-000000000000
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testrg/providers/Microsoft.Network/networkVirtualAppliances/nva/virtualApplianceSites/testsite
```

<span data-ttu-id="4ac26-111">取得虛擬裝置網站資源。</span><span class="sxs-lookup"><span data-stu-id="4ac26-111">Get a Virtual Appliance site resource.</span></span>

### <span data-ttu-id="4ac26-112">範例2</span><span class="sxs-lookup"><span data-stu-id="4ac26-112">Example 2</span></span>
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

<span data-ttu-id="4ac26-113">在網路虛擬裝置中列出虛擬裝置網站資源。</span><span class="sxs-lookup"><span data-stu-id="4ac26-113">List Virtual Appliance site resources in a Network Virtual Appliance.</span></span>


## <span data-ttu-id="4ac26-114">參數</span><span class="sxs-lookup"><span data-stu-id="4ac26-114">PARAMETERS</span></span>

### <span data-ttu-id="4ac26-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ac26-115">-DefaultProfile</span></span>
<span data-ttu-id="4ac26-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4ac26-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ac26-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="4ac26-117">-Name</span></span>
<span data-ttu-id="4ac26-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="4ac26-118">The resource name.</span></span>

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

### <span data-ttu-id="4ac26-119">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="4ac26-119">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="4ac26-120">該網站附加的網路虛擬裝置。</span><span class="sxs-lookup"><span data-stu-id="4ac26-120">The Network Virtual Appliance that the site is attached.</span></span>

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

### <span data-ttu-id="4ac26-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ac26-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ac26-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4ac26-122">The resource group name.</span></span>

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

### <span data-ttu-id="4ac26-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ac26-123">-ResourceId</span></span>
<span data-ttu-id="4ac26-124">虛擬裝置網站的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="4ac26-124">The resource Id of the Virtual Appliance Site.</span></span>

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

### <span data-ttu-id="4ac26-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ac26-125">CommonParameters</span></span>
<span data-ttu-id="4ac26-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4ac26-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ac26-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4ac26-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ac26-128">輸入</span><span class="sxs-lookup"><span data-stu-id="4ac26-128">INPUTS</span></span>

### <span data-ttu-id="4ac26-129">System.object</span><span class="sxs-lookup"><span data-stu-id="4ac26-129">System.String</span></span>

## <span data-ttu-id="4ac26-130">輸出</span><span class="sxs-lookup"><span data-stu-id="4ac26-130">OUTPUTS</span></span>

### <span data-ttu-id="4ac26-131">PSVirtualApplianceSite 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="4ac26-131">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="4ac26-132">筆記</span><span class="sxs-lookup"><span data-stu-id="4ac26-132">NOTES</span></span>

## <span data-ttu-id="4ac26-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="4ac26-133">RELATED LINKS</span></span>