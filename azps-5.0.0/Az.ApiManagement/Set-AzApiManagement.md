---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: c00e8e8d33ef0f7b7b2591287e9bda9bc876e3c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94286191"
---
# <span data-ttu-id="1c1b1-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c1b1-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="1c1b1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1c1b1-102">SYNOPSIS</span></span>
<span data-ttu-id="1c1b1-103">更新 Azure Api 管理服務</span><span class="sxs-lookup"><span data-stu-id="1c1b1-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="1c1b1-104">句法</span><span class="sxs-lookup"><span data-stu-id="1c1b1-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c1b1-105">說明</span><span class="sxs-lookup"><span data-stu-id="1c1b1-105">DESCRIPTION</span></span>

<span data-ttu-id="1c1b1-106">**AzApiManagement** Cmdlet 會更新 Azure API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="1c1b1-107">示例</span><span class="sxs-lookup"><span data-stu-id="1c1b1-107">EXAMPLES</span></span>

### <span data-ttu-id="1c1b1-108">範例1：取得 API 管理服務並將它縮放至 Premium 並新增區域</span><span class="sxs-lookup"><span data-stu-id="1c1b1-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="1c1b1-109">這個範例會取得 Api 管理實例、將它縮放至5個 premium 單位，然後再將額外的三個單元加到 premium 區域。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="1c1b1-110">範例2： (外部 VNET 更新部署) </span><span class="sxs-lookup"><span data-stu-id="1c1b1-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="1c1b1-111">這個命令會更新現有的 API 管理部署，並加入外部 *VpnType* 。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="1c1b1-112">範例3：使用 KeyVault 資源中的秘密來建立和初始化 PsApiManagementCustomHostNameConfiguration 的實例</span><span class="sxs-lookup"><span data-stu-id="1c1b1-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -SystemAssignedIdentity
```

### <span data-ttu-id="1c1b1-113">範例4：更新發行者電子郵件、NotificationSender 電子郵件和組織名稱</span><span class="sxs-lookup"><span data-stu-id="1c1b1-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="1c1b1-114">參數</span><span class="sxs-lookup"><span data-stu-id="1c1b1-114">PARAMETERS</span></span>

### <span data-ttu-id="1c1b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c1b1-115">-AsJob</span></span>
<span data-ttu-id="1c1b1-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="1c1b1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1c1b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c1b1-117">-DefaultProfile</span></span>
<span data-ttu-id="1c1b1-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c1b1-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c1b1-119">-InputObject</span></span>
<span data-ttu-id="1c1b1-120">ApiManagement 實例。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-120">The ApiManagement instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1b1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c1b1-121">-PassThru</span></span>
<span data-ttu-id="1c1b1-122">如果操作成功，則會將更新的 PsApiManagement 傳送到管線。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="1c1b1-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1c1b1-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="1c1b1-124">針對此伺服器產生並指派 Azure Active Directory 身分識別，以搭配諸如 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="1c1b1-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1c1b1-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="1c1b1-126">將使用者身分識別指派給此伺服器，以搭配諸如 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c1b1-127">-確認</span><span class="sxs-lookup"><span data-stu-id="1c1b1-127">-Confirm</span></span>
<span data-ttu-id="1c1b1-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1b1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c1b1-129">-WhatIf</span></span>
<span data-ttu-id="1c1b1-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c1b1-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c1b1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c1b1-132">CommonParameters</span></span>
<span data-ttu-id="1c1b1-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c1b1-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c1b1-135">輸入</span><span class="sxs-lookup"><span data-stu-id="1c1b1-135">INPUTS</span></span>

### <span data-ttu-id="1c1b1-136">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1c1b1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1c1b1-137">OUTPUTS</span></span>

### <span data-ttu-id="1c1b1-138">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="1c1b1-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1c1b1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1c1b1-139">NOTES</span></span>

## <span data-ttu-id="1c1b1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1c1b1-140">RELATED LINKS</span></span>

[<span data-ttu-id="1c1b1-141">AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c1b1-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="1c1b1-142">新-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c1b1-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="1c1b1-143">移除-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c1b1-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
