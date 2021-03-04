---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 2919c007852961386fb1ab444e43d855ced2a8d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904982"
---
# <span data-ttu-id="0384d-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="0384d-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="0384d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0384d-102">SYNOPSIS</span></span>
<span data-ttu-id="0384d-103">獲得與此 VirtualWan 相關聯的所有 VpnServerConfigurations 清單。</span><span class="sxs-lookup"><span data-stu-id="0384d-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="0384d-104">語法</span><span class="sxs-lookup"><span data-stu-id="0384d-104">SYNTAX</span></span>

### <span data-ttu-id="0384d-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="0384d-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0384d-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="0384d-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0384d-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="0384d-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0384d-108">描述</span><span class="sxs-lookup"><span data-stu-id="0384d-108">DESCRIPTION</span></span>
<span data-ttu-id="0384d-109">**Get-AzVirtualWan VpnServerConfiguration Cmdlet** 會返回與此 VirtualWan 相關聯的所有 VpnServerConfiguration 清單。</span><span class="sxs-lookup"><span data-stu-id="0384d-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="0384d-110">i.e. 所有附加至虛擬網站 V一alHubs 下任何 P2S VpnGateway 的 VpnServerConfigurations。</span><span class="sxs-lookup"><span data-stu-id="0384d-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="0384d-111">例子</span><span class="sxs-lookup"><span data-stu-id="0384d-111">EXAMPLES</span></span>

### <span data-ttu-id="0384d-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="0384d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="0384d-113">參數</span><span class="sxs-lookup"><span data-stu-id="0384d-113">PARAMETERS</span></span>

### <span data-ttu-id="0384d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0384d-114">-DefaultProfile</span></span>
<span data-ttu-id="0384d-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0384d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0384d-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="0384d-116">-Name</span></span>
<span data-ttu-id="0384d-117">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="0384d-117">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0384d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0384d-118">-ResourceGroupName</span></span>
<span data-ttu-id="0384d-119">資源組名。</span><span class="sxs-lookup"><span data-stu-id="0384d-119">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0384d-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0384d-120">-ResourceId</span></span>
<span data-ttu-id="0384d-121">虛擬 Wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0384d-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0384d-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="0384d-122">-VirtualWanObject</span></span>
<span data-ttu-id="0384d-123">虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="0384d-123">The virtual wan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0384d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0384d-124">CommonParameters</span></span>
<span data-ttu-id="0384d-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0384d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0384d-126">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="0384d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0384d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="0384d-127">INPUTS</span></span>

### <span data-ttu-id="0384d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="0384d-128">System.String</span></span>
<span data-ttu-id="0384d-129">Microsoft.Azure.Commands.Network.models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="0384d-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="0384d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="0384d-130">OUTPUTS</span></span>

### <span data-ttu-id="0384d-131">Microsoft.Azure.Commands.Network.models.PS VpnServerConfigurationsResponse</span><span class="sxs-lookup"><span data-stu-id="0384d-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="0384d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="0384d-132">NOTES</span></span>

## <span data-ttu-id="0384d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="0384d-133">RELATED LINKS</span></span>
