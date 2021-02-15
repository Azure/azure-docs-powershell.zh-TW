---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualwanvpnserverconfigurationvpnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualWanVpnServerConfigurationVpnProfile.md
ms.openlocfilehash: 5e19f63c0497535c44513c55a28d7117d0783574
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100134982"
---
# <span data-ttu-id="a6e18-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span><span class="sxs-lookup"><span data-stu-id="a6e18-101">Get-AzVirtualWanVpnServerConfigurationVpnProfile</span></span>

## <span data-ttu-id="a6e18-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a6e18-102">SYNOPSIS</span></span>
<span data-ttu-id="a6e18-103">在 VirtualWan-VpnServerConfiguration 層級產生並下載 Vpn 設定檔，以指向網站用戶端設定。</span><span class="sxs-lookup"><span data-stu-id="a6e18-103">Generates and downloads Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="a6e18-104">句法</span><span class="sxs-lookup"><span data-stu-id="a6e18-104">SYNTAX</span></span>

### <span data-ttu-id="a6e18-105">ByVirtualWanNameByVpnServerConfigurationObject (預設) </span><span class="sxs-lookup"><span data-stu-id="a6e18-105">ByVirtualWanNameByVpnServerConfigurationObject (Default)</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6e18-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e18-106">ByVirtualWanNameByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile [-Name <String>] -ResourceGroupName <String>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6e18-107">ByVirtualWanObjectByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a6e18-107">ByVirtualWanObjectByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6e18-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e18-108">ByVirtualWanObjectByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -VirtualWanObject <PSVirtualWan>
 -VpnServerConfigurationId <String> [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6e18-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="a6e18-109">ByVirtualWanResourceIdByVpnServerConfigurationObject</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String>
 -VpnServerConfiguration <PSVpnServerConfiguration> [-AuthenticationMethod <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6e18-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e18-110">ByVirtualWanResourceIdByVpnServerConfigurationResourceId</span></span>
```
Get-AzVirtualWanVpnServerConfigurationVpnProfile -ResourceId <String> -VpnServerConfigurationId <String>
 [-AuthenticationMethod <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6e18-111">說明</span><span class="sxs-lookup"><span data-stu-id="a6e18-111">DESCRIPTION</span></span>
<span data-ttu-id="a6e18-112">**AzVirtualWanVpnServerConfigurationVpnProfile** Cmdlet 可讓您在 VirtualWan-VpnServerConfiguration 階層建立並下載 Vpn 設定檔，以指向網站用戶端設定。</span><span class="sxs-lookup"><span data-stu-id="a6e18-112">The **Get-AzVirtualWanVpnServerConfigurationVpnProfile** cmdlet enables you to generate and download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span> <span data-ttu-id="a6e18-113">若要指向網站連線，請從指向網站用戶端到 Azure P2SVpnGateway，這是必要的。</span><span class="sxs-lookup"><span data-stu-id="a6e18-113">This is required for Point to site connectivity from Point to site client to Azure P2SVpnGateway.</span></span>

## <span data-ttu-id="a6e18-114">示例</span><span class="sxs-lookup"><span data-stu-id="a6e18-114">EXAMPLES</span></span>

### <span data-ttu-id="a6e18-115">範例1</span><span class="sxs-lookup"><span data-stu-id="a6e18-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVirtualWanVpnServerConfigurationVpnProfile -Name WestUsVirtualWan -ResourceGroupName P2SCortexGATesting -VpnServerConfiguration $vpnServerConfig -AuthenticationMethod EAPTLS

ProfileUrl : https://nfvprodsuppby.blob.core.windows.net/vpnprofileimmutable/aa316f33-d0f6-4e61-994a-9aa24c0e5f70/vpnprofile/eb99aa3d-1106-49eb-9644-791c045c5cca/vpnclientconfiguration.zip?sv=2017-04-17&sr=b&sig=kZinevNqW
             qsEAbWAcYiKfUHFxZzh2hwvtb49dfVtUDA%3D&st=2019-10-25T19%3A52%3A36Z&se=2019-10-25T20%3A52%3A36Z&sp=r&fileExtension=.zip
```

<span data-ttu-id="a6e18-116">上述命令會產生並傳回 SAS Url，以供客戶在 VirtualWan-VpnServerConfiguration 層級下載 Vpn 設定檔，以指向網站用戶端設定。</span><span class="sxs-lookup"><span data-stu-id="a6e18-116">The above command will generate and returns SAS Url for customer to download the Vpn profile at VirtualWan-VpnServerConfiguration level for Point to site client setup.</span></span>

## <span data-ttu-id="a6e18-117">參數</span><span class="sxs-lookup"><span data-stu-id="a6e18-117">PARAMETERS</span></span>

### <span data-ttu-id="a6e18-118">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="a6e18-118">-AuthenticationMethod</span></span>
<span data-ttu-id="a6e18-119">驗證方法</span><span class="sxs-lookup"><span data-stu-id="a6e18-119">Authentication Method</span></span>

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

### <span data-ttu-id="a6e18-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6e18-120">-DefaultProfile</span></span>
<span data-ttu-id="a6e18-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a6e18-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6e18-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="a6e18-122">-Name</span></span>
<span data-ttu-id="a6e18-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="a6e18-123">The resource name.</span></span>

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

### <span data-ttu-id="a6e18-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6e18-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6e18-125">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a6e18-125">The resource group name.</span></span>

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

### <span data-ttu-id="a6e18-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6e18-126">-ResourceId</span></span>
<span data-ttu-id="a6e18-127">虛擬 wan 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6e18-127">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="a6e18-128">-VirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="a6e18-128">-VirtualWanObject</span></span>
<span data-ttu-id="a6e18-129">虛擬 wan 物件。</span><span class="sxs-lookup"><span data-stu-id="a6e18-129">The virtual wan object.</span></span>

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

### <span data-ttu-id="a6e18-130">-VpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a6e18-130">-VpnServerConfiguration</span></span>
<span data-ttu-id="a6e18-131">與此 VirtualWan 相關聯的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="a6e18-131">The VpnServerConfiguration with which this VirtualWan is associated.</span></span>

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

### <span data-ttu-id="a6e18-132">-VpnServerConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a6e18-132">-VpnServerConfigurationId</span></span>
<span data-ttu-id="a6e18-133">此虛擬 wan 將關聯之 Vpn server configuraiton 物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a6e18-133">The id of Vpn server configuraiton object this Virtual wan will be associated with.</span></span>

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

### <span data-ttu-id="a6e18-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6e18-134">CommonParameters</span></span>
<span data-ttu-id="a6e18-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a6e18-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6e18-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a6e18-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6e18-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a6e18-137">INPUTS</span></span>

### <span data-ttu-id="a6e18-138">System.object</span><span class="sxs-lookup"><span data-stu-id="a6e18-138">System.String</span></span>
<span data-ttu-id="a6e18-139">PSVirtualWan PSVpnServerConfiguration 中的 []，然後按 [.]</span><span class="sxs-lookup"><span data-stu-id="a6e18-139">Microsoft.Azure.Commands.Network.Models.PSVirtualWan Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a6e18-140">輸出</span><span class="sxs-lookup"><span data-stu-id="a6e18-140">OUTPUTS</span></span>

### <span data-ttu-id="a6e18-141">PSVpnProfileResponse 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="a6e18-141">Microsoft.Azure.Commands.Network.Models.PSVpnProfileResponse</span></span>

## <span data-ttu-id="a6e18-142">筆記</span><span class="sxs-lookup"><span data-stu-id="a6e18-142">NOTES</span></span>

## <span data-ttu-id="a6e18-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6e18-143">RELATED LINKS</span></span>
