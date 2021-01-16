---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278360"
---
# <span data-ttu-id="94498-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="94498-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="94498-102">摘要</span><span class="sxs-lookup"><span data-stu-id="94498-102">SYNOPSIS</span></span>
<span data-ttu-id="94498-103">取得與此 VirtualWan 相關聯之所有 VpnServerConfigurations 的清單。</span><span class="sxs-lookup"><span data-stu-id="94498-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="94498-104">句法</span><span class="sxs-lookup"><span data-stu-id="94498-104">SYNTAX</span></span>

### <span data-ttu-id="94498-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="94498-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94498-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="94498-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94498-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="94498-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94498-108">說明</span><span class="sxs-lookup"><span data-stu-id="94498-108">DESCRIPTION</span></span>
<span data-ttu-id="94498-109">**AzVirtualWanVpnServerConfiguration** Cmdlet 會傳回與此 VirtualWan 關聯的所有 VpnServerConfigurations 清單。</span><span class="sxs-lookup"><span data-stu-id="94498-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="94498-110">亦即，在此 VirtualWan VirutalHubs 下，所有附加至任何 P2SVpnGateways 的 VpnServerConfigurations。</span><span class="sxs-lookup"><span data-stu-id="94498-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="94498-111">示例</span><span class="sxs-lookup"><span data-stu-id="94498-111">EXAMPLES</span></span>

### <span data-ttu-id="94498-112">範例1</span><span class="sxs-lookup"><span data-stu-id="94498-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="94498-113">參數</span><span class="sxs-lookup"><span data-stu-id="94498-113">PARAMETERS</span></span>

### <span data-ttu-id="94498-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94498-114">-DefaultProfile</span></span>
<span data-ttu-id="94498-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="94498-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94498-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="94498-116">-Name</span></span>
<span data-ttu-id="94498-117">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="94498-117">The resource name.</span></span>

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

### <span data-ttu-id="94498-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94498-118">-ResourceGroupName</span></span>
<span data-ttu-id="94498-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94498-119">The resource group name.</span></span>

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

### <span data-ttu-id="94498-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94498-120">-ResourceId</span></span>
<span data-ttu-id="94498-121">虛擬 wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="94498-121">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="94498-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="94498-122">-VirtualWanObject</span></span>
<span data-ttu-id="94498-123">虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="94498-123">The virtual wan object.</span></span>

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

### <span data-ttu-id="94498-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94498-124">CommonParameters</span></span>
<span data-ttu-id="94498-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="94498-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94498-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="94498-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94498-127">輸入</span><span class="sxs-lookup"><span data-stu-id="94498-127">INPUTS</span></span>

### <span data-ttu-id="94498-128">System.object</span><span class="sxs-lookup"><span data-stu-id="94498-128">System.String</span></span>
<span data-ttu-id="94498-129">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="94498-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="94498-130">輸出</span><span class="sxs-lookup"><span data-stu-id="94498-130">OUTPUTS</span></span>

### <span data-ttu-id="94498-131">PSVpnServerConfigurationsResponse 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="94498-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="94498-132">筆記</span><span class="sxs-lookup"><span data-stu-id="94498-132">NOTES</span></span>

## <span data-ttu-id="94498-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="94498-133">RELATED LINKS</span></span>
