---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnServerConfiguration.md
ms.openlocfilehash: 47450d65b883f23bda8141df6be0eb11bc0fa908
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100131298"
---
# <span data-ttu-id="c3704-101">Get-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3704-101">Get-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="c3704-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3704-102">SYNOPSIS</span></span>
<span data-ttu-id="c3704-103">取得指向網站連線的現有 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="c3704-103">Gets an existing VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="c3704-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3704-104">SYNTAX</span></span>

### <span data-ttu-id="c3704-105">ListBySubscriptionId (預設) </span><span class="sxs-lookup"><span data-stu-id="c3704-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnServerConfiguration [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3704-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3704-106">ListByResourceGroupName</span></span>
```
Get-AzVpnServerConfiguration [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3704-107">說明</span><span class="sxs-lookup"><span data-stu-id="c3704-107">DESCRIPTION</span></span>
<span data-ttu-id="c3704-108">**AzVpnServerConfiguration** Cmdlet 會傳回現有的 VpnServerConfiguration，以取得網站連線能力。</span><span class="sxs-lookup"><span data-stu-id="c3704-108">The **Get-AzVpnServerConfiguration** cmdlet returns the existing VpnServerConfiguration for Point to site connectivity.</span></span>

## <span data-ttu-id="c3704-109">示例</span><span class="sxs-lookup"><span data-stu-id="c3704-109">EXAMPLES</span></span>

### <span data-ttu-id="c3704-110">範例1</span><span class="sxs-lookup"><span data-stu-id="c3704-110">Example 1</span></span>
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

<span data-ttu-id="c3704-111">上述命令會取得現有的 VpnServerConfiguration。</span><span class="sxs-lookup"><span data-stu-id="c3704-111">The above command will get the existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="c3704-112">參數</span><span class="sxs-lookup"><span data-stu-id="c3704-112">PARAMETERS</span></span>

### <span data-ttu-id="c3704-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3704-113">-DefaultProfile</span></span>
<span data-ttu-id="c3704-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3704-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3704-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c3704-115">-Name</span></span>
<span data-ttu-id="c3704-116">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="c3704-116">The resource name.</span></span>

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

### <span data-ttu-id="c3704-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3704-117">-ResourceGroupName</span></span>
<span data-ttu-id="c3704-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3704-118">The resource group name.</span></span>

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

### <span data-ttu-id="c3704-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3704-119">CommonParameters</span></span>
<span data-ttu-id="c3704-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3704-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3704-121">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c3704-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3704-122">輸入</span><span class="sxs-lookup"><span data-stu-id="c3704-122">INPUTS</span></span>

### <span data-ttu-id="c3704-123">所有</span><span class="sxs-lookup"><span data-stu-id="c3704-123">None</span></span>

## <span data-ttu-id="c3704-124">輸出</span><span class="sxs-lookup"><span data-stu-id="c3704-124">OUTPUTS</span></span>

### <span data-ttu-id="c3704-125">PSVpnServerConfiguration 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="c3704-125">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="c3704-126">筆記</span><span class="sxs-lookup"><span data-stu-id="c3704-126">NOTES</span></span>

## <span data-ttu-id="c3704-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3704-127">RELATED LINKS</span></span>
