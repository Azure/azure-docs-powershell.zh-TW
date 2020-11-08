---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azp2svpngatewaydetailedconnectionhealth
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzP2sVpnGatewayDetailedConnectionHealth.md
ms.openlocfilehash: 13c74416591318bdebdc869475930111e695d3f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127003"
---
# <span data-ttu-id="e3b50-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="e3b50-101">Get-AzP2sVpnGatewayDetailedConnectionHealth</span></span>

## <span data-ttu-id="e3b50-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e3b50-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b50-103">從 P2SVpnGateway 取得目前指向網站連線的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e3b50-103">Gets the detailed information of current point to site connections from P2SVpnGateway.</span></span>

## <span data-ttu-id="e3b50-104">句法</span><span class="sxs-lookup"><span data-stu-id="e3b50-104">SYNTAX</span></span>

### <span data-ttu-id="e3b50-105">ByP2SVpnGatewayName (預設) </span><span class="sxs-lookup"><span data-stu-id="e3b50-105">ByP2SVpnGatewayName (Default)</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth [-Name <String>] -ResourceGroupName <String>
 -OutputBlobSasUrl <String> [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3b50-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e3b50-106">ByP2SVpnGatewayObject</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -InputObject <PSP2SVpnGateway> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3b50-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e3b50-107">ByP2SVpnGatewayResourceId</span></span>
```
Get-AzP2sVpnGatewayDetailedConnectionHealth -ResourceId <String> -OutputBlobSasUrl <String>
 [-VpnUserNamesFilter <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3b50-108">說明</span><span class="sxs-lookup"><span data-stu-id="e3b50-108">DESCRIPTION</span></span>
<span data-ttu-id="e3b50-109">**AzP2sVpnGatewayDetailedConnectionHealth** Cmdlet 可讓您從 P2SVpnGateway 取得目前指向網站連線的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e3b50-109">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="e3b50-110">客戶需要傳送 SAS url，讓我們可以將這些詳細的健康資訊放在其中。</span><span class="sxs-lookup"><span data-stu-id="e3b50-110">Customer needs to pass SAS url where we can put this detailed health information.</span></span>

## <span data-ttu-id="e3b50-111">示例</span><span class="sxs-lookup"><span data-stu-id="e3b50-111">EXAMPLES</span></span>

### <span data-ttu-id="e3b50-112">範例1</span><span class="sxs-lookup"><span data-stu-id="e3b50-112">Example 1</span></span>
```powershell
PS C:\> $blobSasUrl = New-AzStorageBlobSASToken -Container contp2stesting -Blob emptyfile.txt -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> $blobSasUrl
SignedSasUrl
PS C:\> Get-AzP2sVpnGatewayDetailedConnectionHealth -Name 683482ade8564515aed4b8448c9757ea-westus-gw -ResourceGroupName P2SCortexGATesting -OutputBlobSasUrl $blobSasUrl
SasUrl : SignedSasUrl
```

<span data-ttu-id="e3b50-113">**AzP2sVpnGatewayDetailedConnectionHealth** Cmdlet 可讓您從 P2SVpnGateway 取得目前指向網站連線的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="e3b50-113">The **Get-AzP2sVpnGatewayDetailedConnectionHealth** cmdlet enables you to get the detailed information of current point to site connections from P2SVpnGateway.</span></span> <span data-ttu-id="e3b50-114">客戶可以從已傳送的 SAS url 下載下載健康情況詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e3b50-114">Customer can download health details from passed SAS url download.</span></span> <span data-ttu-id="e3b50-115">這會顯示每個網站連線與使用者名、位元組數、位元組數、已分配 ip 位址等相關的資訊。</span><span class="sxs-lookup"><span data-stu-id="e3b50-115">This will show information of each point to site connection with usernames, bytes in, bytes out, allocated ip address etc.</span></span>

## <span data-ttu-id="e3b50-116">參數</span><span class="sxs-lookup"><span data-stu-id="e3b50-116">PARAMETERS</span></span>

### <span data-ttu-id="e3b50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b50-117">-DefaultProfile</span></span>
<span data-ttu-id="e3b50-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e3b50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b50-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3b50-119">-InputObject</span></span>
<span data-ttu-id="e3b50-120">要修改的 p2s vpn 閘道物件</span><span class="sxs-lookup"><span data-stu-id="e3b50-120">The p2s vpn gateway object to be modified</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b50-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="e3b50-121">-Name</span></span>
<span data-ttu-id="e3b50-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e3b50-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b50-123">-OutputBlobSasUrl</span><span class="sxs-lookup"><span data-stu-id="e3b50-123">-OutputBlobSasUrl</span></span>
<span data-ttu-id="e3b50-124">P2s vpn 連線健康情況將寫入的 OutputBlob Sas url。</span><span class="sxs-lookup"><span data-stu-id="e3b50-124">OutputBlob Sas url to which the p2s vpn connection health will be written.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b50-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b50-125">-ResourceGroupName</span></span>
<span data-ttu-id="e3b50-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e3b50-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b50-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3b50-127">-ResourceId</span></span>
<span data-ttu-id="e3b50-128">要修改之 P2SVpnGateway 的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3b50-128">The Azure resource ID of the P2SVpnGateway to be modified.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b50-129">-VpnUserNamesFilter</span><span class="sxs-lookup"><span data-stu-id="e3b50-129">-VpnUserNamesFilter</span></span>
<span data-ttu-id="e3b50-130">要篩選的 P2S vpn 使用者名稱清單。</span><span class="sxs-lookup"><span data-stu-id="e3b50-130">The list of P2S vpn user names to filter.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b50-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b50-131">CommonParameters</span></span>
<span data-ttu-id="e3b50-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e3b50-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b50-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e3b50-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b50-134">輸入</span><span class="sxs-lookup"><span data-stu-id="e3b50-134">INPUTS</span></span>

### <span data-ttu-id="e3b50-135">System.object</span><span class="sxs-lookup"><span data-stu-id="e3b50-135">System.String</span></span>
<span data-ttu-id="e3b50-136">PSP2SVpnGateway 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3b50-136">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>

## <span data-ttu-id="e3b50-137">輸出</span><span class="sxs-lookup"><span data-stu-id="e3b50-137">OUTPUTS</span></span>

### <span data-ttu-id="e3b50-138">PSP2SVpnConnectionHealth 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e3b50-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnConnectionHealth</span></span>

## <span data-ttu-id="e3b50-139">筆記</span><span class="sxs-lookup"><span data-stu-id="e3b50-139">NOTES</span></span>

## <span data-ttu-id="e3b50-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="e3b50-140">RELATED LINKS</span></span>