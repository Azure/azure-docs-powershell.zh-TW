---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfiguration.md
ms.openlocfilehash: 6124b3ddb862254d11bd141560a682bb91bb7fb7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138341"
---
# <span data-ttu-id="dedfd-101">Get-AzVirtualWanVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="dedfd-101">Get-AzVirtualWanVpnServerConfiguration</span></span>

## <span data-ttu-id="dedfd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dedfd-102">SYNOPSIS</span></span>
<span data-ttu-id="dedfd-103">取得與此 VirtualWan 相關聯之所有 VpnServerConfigurations 的清單。</span><span class="sxs-lookup"><span data-stu-id="dedfd-103">Gets the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span>

## <span data-ttu-id="dedfd-104">句法</span><span class="sxs-lookup"><span data-stu-id="dedfd-104">SYNTAX</span></span>

### <span data-ttu-id="dedfd-105">ByVirtualWanName (預設) </span><span class="sxs-lookup"><span data-stu-id="dedfd-105">ByVirtualWanName (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dedfd-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="dedfd-106">ByVirtualWanObject</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String>
 -VirtualWanObject <PSVirtualWan> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dedfd-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="dedfd-107">ByVirtualWanResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfiguration [-Name <String>] -ResourceGroupName <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dedfd-108">說明</span><span class="sxs-lookup"><span data-stu-id="dedfd-108">DESCRIPTION</span></span>
<span data-ttu-id="dedfd-109">**AzVirtualWanVpnServerConfiguration** Cmdlet 會傳回與此 VirtualWan 關聯的所有 VpnServerConfigurations 清單。</span><span class="sxs-lookup"><span data-stu-id="dedfd-109">The **Get-AzVirtualWanVpnServerConfiguration** cmdlet will return the list of all VpnServerConfigurations that are associated with this VirtualWan.</span></span> <span data-ttu-id="dedfd-110">亦即，在此 VirtualWan VirutalHubs 下，所有附加至任何 P2SVpnGateways 的 VpnServerConfigurations。</span><span class="sxs-lookup"><span data-stu-id="dedfd-110">i.e. All the VpnServerConfigurations which are attached to any P2SVpnGateways under VirutalHubs of this VirtualWan.</span></span>

## <span data-ttu-id="dedfd-111">示例</span><span class="sxs-lookup"><span data-stu-id="dedfd-111">EXAMPLES</span></span>

### <span data-ttu-id="dedfd-112">範例1</span><span class="sxs-lookup"><span data-stu-id="dedfd-112">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfiguration -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting

VpnServerConfigurationResourceIds : [
                                      "/subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/WestUsConfig"                           ]
```

## <span data-ttu-id="dedfd-113">參數</span><span class="sxs-lookup"><span data-stu-id="dedfd-113">PARAMETERS</span></span>

### <span data-ttu-id="dedfd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dedfd-114">-DefaultProfile</span></span>
<span data-ttu-id="dedfd-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="dedfd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dedfd-116">-名稱</span><span class="sxs-lookup"><span data-stu-id="dedfd-116">-Name</span></span>
<span data-ttu-id="dedfd-117">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="dedfd-117">The resource name.</span></span>

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

### <span data-ttu-id="dedfd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dedfd-118">-ResourceGroupName</span></span>
<span data-ttu-id="dedfd-119">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="dedfd-119">The resource group name.</span></span>

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

### <span data-ttu-id="dedfd-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dedfd-120">-ResourceId</span></span>
<span data-ttu-id="dedfd-121">虛擬 wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="dedfd-121">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="dedfd-122">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="dedfd-122">-VirtualWanObject</span></span>
<span data-ttu-id="dedfd-123">虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="dedfd-123">The virtual wan object.</span></span>

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

### <span data-ttu-id="dedfd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dedfd-124">CommonParameters</span></span>
<span data-ttu-id="dedfd-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dedfd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dedfd-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dedfd-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dedfd-127">輸入</span><span class="sxs-lookup"><span data-stu-id="dedfd-127">INPUTS</span></span>

### <span data-ttu-id="dedfd-128">System.object</span><span class="sxs-lookup"><span data-stu-id="dedfd-128">System.String</span></span>
<span data-ttu-id="dedfd-129">PSVirtualWan 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dedfd-129">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="dedfd-130">輸出</span><span class="sxs-lookup"><span data-stu-id="dedfd-130">OUTPUTS</span></span>

### <span data-ttu-id="dedfd-131">PSVpnServerConfigurationsResponse 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="dedfd-131">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfigurationsResponse</span></span>

## <span data-ttu-id="dedfd-132">筆記</span><span class="sxs-lookup"><span data-stu-id="dedfd-132">NOTES</span></span>

## <span data-ttu-id="dedfd-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="dedfd-133">RELATED LINKS</span></span>
