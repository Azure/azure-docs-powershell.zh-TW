---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98287051"
---
# <span data-ttu-id="11786-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="11786-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="11786-102">摘要</span><span class="sxs-lookup"><span data-stu-id="11786-102">SYNOPSIS</span></span>
<span data-ttu-id="11786-103">取得指向網站連線的現有 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="11786-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="11786-104">句法</span><span class="sxs-lookup"><span data-stu-id="11786-104">SYNTAX</span></span>

### <span data-ttu-id="11786-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="11786-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11786-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11786-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11786-107">說明</span><span class="sxs-lookup"><span data-stu-id="11786-107">DESCRIPTION</span></span>
<span data-ttu-id="11786-108">**AzVpnServerConfiguration** Cmdlet 會傳回現有的 VpnServerConfiguration，以取得網站連線能力。</span><span class="sxs-lookup"><span data-stu-id="11786-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="11786-109">示例</span><span class="sxs-lookup"><span data-stu-id="11786-109">EXAMPLES</span></span>

### <span data-ttu-id="11786-110">範例1</span><span class="sxs-lookup"><span data-stu-id="11786-110">Example 1</span></span>
```powershell
PS C:\> Get-AzVpnServerConfiguration -ResourceGroupName P2SCortexGATesting -Name test1config

ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="11786-111">上述命令會取得現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="11786-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="11786-112">參數</span><span class="sxs-lookup"><span data-stu-id="11786-112">PARAMETERS</span></span>

### <span data-ttu-id="11786-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11786-113">-DefaultProfile</span></span>
<span data-ttu-id="11786-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="11786-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11786-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="11786-115">-Name</span></span>
<span data-ttu-id="11786-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="11786-116">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnServerConfigurationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11786-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11786-117">-ResourceGroupName</span></span>
<span data-ttu-id="11786-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="11786-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11786-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11786-119">CommonParameters</span></span>
<span data-ttu-id="11786-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="11786-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11786-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="11786-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11786-122">輸入</span><span class="sxs-lookup"><span data-stu-id="11786-122">INPUTS</span></span>

### <span data-ttu-id="11786-123">所有</span><span class="sxs-lookup"><span data-stu-id="11786-123">None</span></span>

## <span data-ttu-id="11786-124">輸出</span><span class="sxs-lookup"><span data-stu-id="11786-124">OUTPUTS</span></span>

### <span data-ttu-id="11786-125">PSVpnServerConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="11786-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="11786-126">筆記</span><span class="sxs-lookup"><span data-stu-id="11786-126">NOTES</span></span>

## <span data-ttu-id="11786-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="11786-127">RELATED LINKS</span></span>
