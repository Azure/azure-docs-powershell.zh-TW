---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: e0a39aac53b13356eb9719cad6e2ade11483cfe7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909537"
---
# <span data-ttu-id="b8900-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="b8900-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="b8900-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b8900-102">SYNOPSIS</span></span>
<span data-ttu-id="b8900-103">在指向網站用戶端設定VirtualWan-VpnServerConfiguration層級產生和下載 Vpn 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b8900-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="b8900-104">語法</span><span class="sxs-lookup"><span data-stu-id="b8900-104">SYNTAX</span></span>

### <span data-ttu-id="b8900-105">ByVirtualWanNameBy VpnServerConfigurationObject (預設) </span><span class="sxs-lookup"><span data-stu-id="b8900-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8900-106">ByVirtualWanNameBy VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b8900-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8900-107">ByVirtualWanObjectBy VpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b8900-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8900-108">ByVirtualWanObjectBy VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b8900-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8900-109">ByVirtualWanResourceIdBy VpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="b8900-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8900-110">ByVirtualWanResourceIdBy VpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="b8900-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8900-111">描述</span><span class="sxs-lookup"><span data-stu-id="b8900-111">DESCRIPTION</span></span>
<span data-ttu-id="b8900-112">**Get-AzVirtualWan VpnServerConfiguration VpnProfile** Cmdlet 可讓您在 VirtualWan-VpnServerConfiguration 層級產生並下載 Vpn 設定檔，以設定指向網站用戶端。</span><span class="sxs-lookup"><span data-stu-id="b8900-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="b8900-113">從點到網站用戶端到 Azure P2S VpnGateway 的點到網站連接是必填項。</span><span class="sxs-lookup"><span data-stu-id="b8900-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="b8900-114">例子</span><span class="sxs-lookup"><span data-stu-id="b8900-114">EXAMPLES</span></span>

### <span data-ttu-id="b8900-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="b8900-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="b8900-116">上述命令會針對指向網站用戶端設定，產生並VirtualWan-VpnServerConfiguration客戶下載 VPN 設定檔的 SAS URL。</span><span class="sxs-lookup"><span data-stu-id="b8900-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="b8900-117">參數</span><span class="sxs-lookup"><span data-stu-id="b8900-117">PARAMETERS</span></span>

### <span data-ttu-id="b8900-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="b8900-118">-AuthenticationMethod</span></span>
<span data-ttu-id="b8900-119">驗證方法</span><span class="sxs-lookup"><span data-stu-id="b8900-119">Authentication Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8900-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8900-120">-DefaultProfile</span></span>
<span data-ttu-id="b8900-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b8900-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8900-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8900-122">-Name</span></span>
<span data-ttu-id="b8900-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="b8900-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8900-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8900-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8900-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="b8900-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanNameByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8900-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8900-126">-ResourceId</span></span>
<span data-ttu-id="b8900-127">虛擬 Wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8900-127">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanResourceIdByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8900-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="b8900-128">-VirtualWanObject</span></span>
<span data-ttu-id="b8900-129">虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="b8900-129">The virtual wan object.</span></span>

```yaml
Type: PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8900-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8900-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="b8900-131">與此 VirtualWan 相關聯的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="b8900-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationObject, ByVirtualWanObjectByVpnServerConfigurationObject, ByVirtualWanResourceIdByVpnServerConfigurationObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8900-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="b8900-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="b8900-133">與這個虛擬 Wan 相關聯的 Vpn 伺服器 configuraiton 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b8900-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualWanNameByVpnServerConfigurationResourceId, ByVirtualWanObjectByVpnServerConfigurationResourceId, ByVirtualWanResourceIdByVpnServerConfigurationResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8900-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8900-134">CommonParameters</span></span>
<span data-ttu-id="b8900-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b8900-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8900-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b8900-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8900-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b8900-137">INPUTS</span></span>

### <span data-ttu-id="b8900-138">System.String</span><span class="sxs-lookup"><span data-stu-id="b8900-138">System.String</span></span>
<span data-ttu-id="b8900-139">Microsoft.Azure.Commands.network.models.PSVirtualWan Microsoft.Azure.Commands.network.models.PS VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8900-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="b8900-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b8900-140">OUTPUTS</span></span>

### <span data-ttu-id="b8900-141">Microsoft.Azure.Commands.Network.models.PS VpnProfileResponse</span><span class="sxs-lookup"><span data-stu-id="b8900-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="b8900-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b8900-142">NOTES</span></span>

## <span data-ttu-id="b8900-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8900-143">RELATED LINKS</span></span>
