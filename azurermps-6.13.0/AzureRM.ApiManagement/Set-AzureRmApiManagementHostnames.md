---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementhostnames
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: 7093b51ffee3f0ad635da7a6c0b63d26e93e5f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447517"
---
# <span data-ttu-id="69dec-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="69dec-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="69dec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69dec-102">SYNOPSIS</span></span>
<span data-ttu-id="69dec-103">針對 API 管理服務 proxy 或入口網站設定自訂主機名稱的配置。</span><span class="sxs-lookup"><span data-stu-id="69dec-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69dec-104">句法</span><span class="sxs-lookup"><span data-stu-id="69dec-104">SYNTAX</span></span>

### <span data-ttu-id="69dec-105">SetSpecificService (預設) </span><span class="sxs-lookup"><span data-stu-id="69dec-105">SetSpecificService (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69dec-106">SetFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="69dec-106">SetFromPsApiManagementInstance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69dec-107">說明</span><span class="sxs-lookup"><span data-stu-id="69dec-107">DESCRIPTION</span></span>
<span data-ttu-id="69dec-108">AzureRmApiManagementHostnames Cmdlet 會將自訂主機名稱 **設定** 套用至 API 管理服務 proxy 或入口網站。</span><span class="sxs-lookup"><span data-stu-id="69dec-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="69dec-109">示例</span><span class="sxs-lookup"><span data-stu-id="69dec-109">EXAMPLES</span></span>

### <span data-ttu-id="69dec-110">範例1：設定 proxy 與入口網站的自訂主機名稱配置</span><span class="sxs-lookup"><span data-stu-id="69dec-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="69dec-111">這個命令會設定 proxy 與入口網站的自訂主機名稱配置。</span><span class="sxs-lookup"><span data-stu-id="69dec-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="69dec-112">範例2：設定 proxy 與入口網站的自訂主機名稱</span><span class="sxs-lookup"><span data-stu-id="69dec-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="69dec-113">這個範例會設定 proxy 與入口網站的自訂主機名稱。</span><span class="sxs-lookup"><span data-stu-id="69dec-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="69dec-114">您必須匯入對應的憑證，然後套用自訂的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="69dec-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="69dec-115">參數</span><span class="sxs-lookup"><span data-stu-id="69dec-115">PARAMETERS</span></span>

### <span data-ttu-id="69dec-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="69dec-116">-ApiManagement</span></span>
<span data-ttu-id="69dec-117">指定此 Cmdlet 取得 *PortalHostnameConfiguration* 和 *ProxyHostnameConfiguration* 參數的 **PsApiManagement** 實例。</span><span class="sxs-lookup"><span data-stu-id="69dec-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: SetFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69dec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69dec-118">-DefaultProfile</span></span>
<span data-ttu-id="69dec-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="69dec-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69dec-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="69dec-120">-Name</span></span>
<span data-ttu-id="69dec-121">指定 API 管理實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="69dec-121">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69dec-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69dec-122">-PassThru</span></span>
<span data-ttu-id="69dec-123">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="69dec-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="69dec-124">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="69dec-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69dec-125">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="69dec-125">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="69dec-126">指定自訂入口網站主機名稱的配置。</span><span class="sxs-lookup"><span data-stu-id="69dec-126">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="69dec-127">將 $null 傳遞到 Cmdlet 會設定預設的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="69dec-127">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69dec-128">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="69dec-128">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="69dec-129">指定自訂 proxy 主機名稱的配置。</span><span class="sxs-lookup"><span data-stu-id="69dec-129">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="69dec-130">傳遞 $null 會設定預設的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="69dec-130">Passing $null sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69dec-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69dec-131">-ResourceGroupName</span></span>
<span data-ttu-id="69dec-132">指定 API 管理實例所在之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="69dec-132">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69dec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69dec-133">CommonParameters</span></span>
<span data-ttu-id="69dec-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69dec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69dec-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69dec-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69dec-136">輸入</span><span class="sxs-lookup"><span data-stu-id="69dec-136">INPUTS</span></span>

### <span data-ttu-id="69dec-137">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="69dec-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="69dec-138">參數： ApiManagement (ByValue) </span><span class="sxs-lookup"><span data-stu-id="69dec-138">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="69dec-139">System.object</span><span class="sxs-lookup"><span data-stu-id="69dec-139">System.String</span></span>

### <span data-ttu-id="69dec-140">PsApiManagementHostnameConfiguration 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="69dec-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="69dec-141">輸出</span><span class="sxs-lookup"><span data-stu-id="69dec-141">OUTPUTS</span></span>

### <span data-ttu-id="69dec-142">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="69dec-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="69dec-143">筆記</span><span class="sxs-lookup"><span data-stu-id="69dec-143">NOTES</span></span>

## <span data-ttu-id="69dec-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="69dec-144">RELATED LINKS</span></span>

[<span data-ttu-id="69dec-145">匯入-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="69dec-145">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="69dec-146">新-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="69dec-146">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)


