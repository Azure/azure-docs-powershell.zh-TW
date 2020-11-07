---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: de25e096be96e54d2a8aa18f24bf9915a2f16538
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959488"
---
# <span data-ttu-id="15340-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="15340-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="15340-102">摘要</span><span class="sxs-lookup"><span data-stu-id="15340-102">SYNOPSIS</span></span>
<span data-ttu-id="15340-103">取得與此 VirtualWan 相關聯之所有 VpnServerConfigurations 的清單。</span><span class="sxs-lookup"><span data-stu-id="15340-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="15340-104">句法</span><span class="sxs-lookup"><span data-stu-id="15340-104">SYNTAX</span></span>

### <span data-ttu-id="15340-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="15340-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15340-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="15340-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15340-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="15340-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15340-108">說明</span><span class="sxs-lookup"><span data-stu-id="15340-108">DESCRIPTION</span></span>
<span data-ttu-id="15340-109">**AzVirtualWanVpnServerConfiguration** Cmdlet 會傳回與此 VirtualWan 關聯的所有 VpnServerConfigurations 清單。</span><span class="sxs-lookup"><span data-stu-id="15340-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="15340-110">亦即，在此 VirtualWan VirutalHubs 下，所有附加至任何 P2SVpnGateways 的 VpnServerConfigurations。</span><span class="sxs-lookup"><span data-stu-id="15340-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="15340-111">示例</span><span class="sxs-lookup"><span data-stu-id="15340-111">EXAMPLES</span></span>

### <span data-ttu-id="15340-112">範例1</span><span class="sxs-lookup"><span data-stu-id="15340-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="15340-113">參數</span><span class="sxs-lookup"><span data-stu-id="15340-113">PARAMETERS</span></span>

### <span data-ttu-id="15340-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15340-114">-DefaultProfile</span></span>
<span data-ttu-id="15340-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="15340-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15340-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="15340-116">-Name</span></span>
<span data-ttu-id="15340-117">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="15340-117">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15340-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15340-118">-ResourceGroupName</span></span>
<span data-ttu-id="15340-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="15340-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15340-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15340-120">-ResourceId</span></span>
<span data-ttu-id="15340-121">虛擬 wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="15340-121">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15340-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="15340-122">-VirtualWanObject</span></span>
<span data-ttu-id="15340-123">虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="15340-123">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15340-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15340-124">CommonParameters</span></span>
<span data-ttu-id="15340-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="15340-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15340-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="15340-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15340-127">輸入</span><span class="sxs-lookup"><span data-stu-id="15340-127">INPUTS</span></span>

### <span data-ttu-id="15340-128">System.object</span><span class="sxs-lookup"><span data-stu-id="15340-128">System.String</span></span>
<span data-ttu-id="15340-129">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="15340-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="15340-130">輸出</span><span class="sxs-lookup"><span data-stu-id="15340-130">OUTPUTS</span></span>

### <span data-ttu-id="15340-131">PSVpnServerConfigurationsResponse 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="15340-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="15340-132">筆記</span><span class="sxs-lookup"><span data-stu-id="15340-132">NOTES</span></span>

## <span data-ttu-id="15340-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="15340-133">RELATED LINKS</span></span>
