---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624945"
---
# <span data-ttu-id="a2fd9-101">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="a2fd9-101">Set-AzureRmApiManagement</span></span>

## <span data-ttu-id="a2fd9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a2fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="a2fd9-103">更新 Azure Api 管理服務</span><span class="sxs-lookup"><span data-stu-id="a2fd9-103">Updates an Azure Api Management service</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2fd9-104">句法</span><span class="sxs-lookup"><span data-stu-id="a2fd9-104">SYNTAX</span></span>

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2fd9-105">說明</span><span class="sxs-lookup"><span data-stu-id="a2fd9-105">DESCRIPTION</span></span>

<span data-ttu-id="a2fd9-106">**AzureRmApiManagement** Cmdlet 會更新 Azure API 管理服務。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-106">The **Set-AzureRmApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="a2fd9-107">示例</span><span class="sxs-lookup"><span data-stu-id="a2fd9-107">EXAMPLES</span></span>

### <span data-ttu-id="a2fd9-108">範例1取得 API 管理服務，並將它縮放至 [特優] 和 [新增區域]</span><span class="sxs-lookup"><span data-stu-id="a2fd9-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="a2fd9-109">這個範例會取得 Api 管理實例、將它縮放至5個 premium 單位，然後再將額外的三個單元加到 premium 區域。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="a2fd9-110">範例2： (外部 VNET 更新部署) </span><span class="sxs-lookup"><span data-stu-id="a2fd9-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="a2fd9-111">這個命令會更新現有的 API 管理部署，並加入外部 *VpnType* 。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="a2fd9-112">範例3：使用 KeyVault 資源中的秘密來建立和初始化 PsApiManagementCustomHostNameConfiguration 的實例</span><span class="sxs-lookup"><span data-stu-id="a2fd9-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## <span data-ttu-id="a2fd9-113">參數</span><span class="sxs-lookup"><span data-stu-id="a2fd9-113">PARAMETERS</span></span>

### <span data-ttu-id="a2fd9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2fd9-114">-AsJob</span></span>
<span data-ttu-id="a2fd9-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a2fd9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2fd9-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a2fd9-116">-AssignIdentity</span></span>
<span data-ttu-id="a2fd9-117">針對此伺服器產生並指派 Azure Active Directory 身分識別，以搭配諸如 Azure KeyVault 等金鑰管理服務使用。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-117">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a2fd9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2fd9-118">-DefaultProfile</span></span>
<span data-ttu-id="a2fd9-119">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2fd9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2fd9-120">-InputObject</span></span>
<span data-ttu-id="a2fd9-121">ApiManagement 實例。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-121">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="a2fd9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2fd9-122">-PassThru</span></span>
<span data-ttu-id="a2fd9-123">如果操作成功，則會將更新的 PsApiManagement 傳送到管線。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-123">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="a2fd9-124">-確認</span><span class="sxs-lookup"><span data-stu-id="a2fd9-124">-Confirm</span></span>
<span data-ttu-id="a2fd9-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2fd9-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2fd9-126">-WhatIf</span></span>
<span data-ttu-id="a2fd9-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2fd9-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2fd9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2fd9-129">CommonParameters</span></span>
<span data-ttu-id="a2fd9-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2fd9-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2fd9-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a2fd9-132">INPUTS</span></span>

### <span data-ttu-id="a2fd9-133">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="a2fd9-134">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a2fd9-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="a2fd9-135">輸出</span><span class="sxs-lookup"><span data-stu-id="a2fd9-135">OUTPUTS</span></span>

### <span data-ttu-id="a2fd9-136">PsApiManagement 中的 ApiManagement。</span><span class="sxs-lookup"><span data-stu-id="a2fd9-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a2fd9-137">筆記</span><span class="sxs-lookup"><span data-stu-id="a2fd9-137">NOTES</span></span>

## <span data-ttu-id="a2fd9-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="a2fd9-138">RELATED LINKS</span></span>

[<span data-ttu-id="a2fd9-139">AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="a2fd9-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="a2fd9-140">新-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="a2fd9-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="a2fd9-141">移除-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="a2fd9-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)
