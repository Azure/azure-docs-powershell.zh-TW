---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorfrontendendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorFrontendEndpointObject.md
ms.openlocfilehash: 638617cfe55e01121b46c7fe283d3664948e76b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93443828"
---
# <span data-ttu-id="f6326-101">New-AzureRmFrontDoorFrontendEndpointObject</span><span class="sxs-lookup"><span data-stu-id="f6326-101">New-AzureRmFrontDoorFrontendEndpointObject</span></span>

## <span data-ttu-id="f6326-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6326-102">SYNOPSIS</span></span>
<span data-ttu-id="f6326-103">建立用來建立前門的 PSFrontendEndpoint 物件</span><span class="sxs-lookup"><span data-stu-id="f6326-103">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6326-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6326-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorFrontendEndpointObject -Name <String> -HostName <String>
 [-SessionAffinityEnabledState <PSEnabledState>] [-SessionAffinityTtlInSeconds <Int32>]
 [-WebApplicationFirewallPolicyLink <String>] [-CertificateSource <PSCertificateSource>]
 [-ProtocolType <PSProtocolType>] [-Vault <String>] [-SecretName <String>] [-SecretVersion <String>]
 [-CertificateType <PSCertificateType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6326-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6326-105">DESCRIPTION</span></span>
<span data-ttu-id="f6326-106">建立用來建立前門的 PSFrontendEndpoint 物件</span><span class="sxs-lookup"><span data-stu-id="f6326-106">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="f6326-107">示例</span><span class="sxs-lookup"><span data-stu-id="f6326-107">EXAMPLES</span></span>

### <span data-ttu-id="f6326-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f6326-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorFrontendEndpointObject -Name "frontendendpoint1" -HostName $hostName


HostName                         : frontdoor5.azurefd.net
SessionAffinityEnabledState      : Disabled
SessionAffinityTtlSeconds        : 0
WebApplicationFirewallPolicyLink :
Backends                         :
CustomHttpsProvisioningState     :
CustomHttpsProvisioningSubstate  :
CertificateSource                : AzureKeyVault
ProtocolType                     : ServerNameIndication
Vault                            :
SecretName                       :
SecretVersion                    :
CertificateType                  : Shared
ResourceState                    :
Id                               :
Name                             : frontendendpoint1
Type                             :
```

<span data-ttu-id="f6326-109">建立用來建立前門的 PSFrontendEndpoint 物件</span><span class="sxs-lookup"><span data-stu-id="f6326-109">Create a PSFrontendEndpoint Object for Front Door creation</span></span>

## <span data-ttu-id="f6326-110">參數</span><span class="sxs-lookup"><span data-stu-id="f6326-110">PARAMETERS</span></span>

### <span data-ttu-id="f6326-111">-CertificateSource</span><span class="sxs-lookup"><span data-stu-id="f6326-111">-CertificateSource</span></span>
<span data-ttu-id="f6326-112">SSL 憑證的來源</span><span class="sxs-lookup"><span data-stu-id="f6326-112">The source of the SSL certificate</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateSource
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, FrontDoor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-113">-CertificateType</span><span class="sxs-lookup"><span data-stu-id="f6326-113">-CertificateType</span></span>
<span data-ttu-id="f6326-114">用於安全連線至 frontendEndpoint 的憑證類型</span><span class="sxs-lookup"><span data-stu-id="f6326-114">the type of the certificate used for secure connections to a frontendEndpoint</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSCertificateType
Parameter Sets: (All)
Aliases:
Accepted values: Shared, Dedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6326-115">-DefaultProfile</span></span>
<span data-ttu-id="f6326-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6326-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-117">-HostName</span><span class="sxs-lookup"><span data-stu-id="f6326-117">-HostName</span></span>
<span data-ttu-id="f6326-118">FrontendEndpoint 的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="f6326-118">The host name of the frontendEndpoint.</span></span>
<span data-ttu-id="f6326-119">必須是功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="f6326-119">Must be a domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6326-120">-Name</span></span>
<span data-ttu-id="f6326-121">前端端點名稱。</span><span class="sxs-lookup"><span data-stu-id="f6326-121">Frontend endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-122">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="f6326-122">-ProtocolType</span></span>
<span data-ttu-id="f6326-123">用於安全傳遞的 TLS 延伸通訊協定</span><span class="sxs-lookup"><span data-stu-id="f6326-123">The TLS extension protocol that is used for secure delivery</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSProtocolType
Parameter Sets: (All)
Aliases:
Accepted values: ServerNameIndication, IPBased

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-124">-SecretName</span><span class="sxs-lookup"><span data-stu-id="f6326-124">-SecretName</span></span>
<span data-ttu-id="f6326-125">代表完整證書 PFX 的主要保存庫密碼名稱</span><span class="sxs-lookup"><span data-stu-id="f6326-125">The name of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-126">-SecretVersion</span><span class="sxs-lookup"><span data-stu-id="f6326-126">-SecretVersion</span></span>
<span data-ttu-id="f6326-127">代表完整證書 PFX 的主要保存庫密碼版本</span><span class="sxs-lookup"><span data-stu-id="f6326-127">The version of the Key Vault secret representing the full certificate PFX</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-128">-SessionAffinityEnabledState</span><span class="sxs-lookup"><span data-stu-id="f6326-128">-SessionAffinityEnabledState</span></span>
<span data-ttu-id="f6326-129">是否允許在這個主機上進行會話關聯。</span><span class="sxs-lookup"><span data-stu-id="f6326-129">Whether to allow session affinity on this host.</span></span>
<span data-ttu-id="f6326-130">已停用預設值</span><span class="sxs-lookup"><span data-stu-id="f6326-130">Default value is Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-131">-SessionAffinityTtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="f6326-131">-SessionAffinityTtlInSeconds</span></span>
<span data-ttu-id="f6326-132">要在會話關聯的秒數中使用的 TTL （如果適用的話）。</span><span class="sxs-lookup"><span data-stu-id="f6326-132">The TTL to use in seconds for session affinity, if applicable.</span></span> <span data-ttu-id="f6326-133">預設值為0</span><span class="sxs-lookup"><span data-stu-id="f6326-133">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-134">-保存庫</span><span class="sxs-lookup"><span data-stu-id="f6326-134">-Vault</span></span>
<span data-ttu-id="f6326-135">包含 SSL 憑證的主要保存庫</span><span class="sxs-lookup"><span data-stu-id="f6326-135">The Key Vault containing the SSL certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-136">-WebApplicationFirewallPolicyLink</span><span class="sxs-lookup"><span data-stu-id="f6326-136">-WebApplicationFirewallPolicyLink</span></span>
<span data-ttu-id="f6326-137">每個主機的 Web 應用程式防火牆原則的資源識別碼（如果適用的話） () </span><span class="sxs-lookup"><span data-stu-id="f6326-137">The resource id of Web Application Firewall policy for each host (if applicable)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6326-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6326-138">CommonParameters</span></span>
<span data-ttu-id="f6326-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6326-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6326-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6326-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6326-141">輸入</span><span class="sxs-lookup"><span data-stu-id="f6326-141">INPUTS</span></span>

### <span data-ttu-id="f6326-142">所有</span><span class="sxs-lookup"><span data-stu-id="f6326-142">None</span></span>

## <span data-ttu-id="f6326-143">輸出</span><span class="sxs-lookup"><span data-stu-id="f6326-143">OUTPUTS</span></span>

### <span data-ttu-id="f6326-144">PSFrontendEndpoint 中的 FrontDoor。</span><span class="sxs-lookup"><span data-stu-id="f6326-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint</span></span>

## <span data-ttu-id="f6326-145">筆記</span><span class="sxs-lookup"><span data-stu-id="f6326-145">NOTES</span></span>

## <span data-ttu-id="f6326-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6326-146">RELATED LINKS</span></span>

<span data-ttu-id="f6326-147">[新-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="f6326-147">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
