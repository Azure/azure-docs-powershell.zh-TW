---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: e5dd9da25bfa2c27bd605dc80b04f8e47fb7f95b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904953"
---
# <span data-ttu-id="47364-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="47364-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="47364-102">簡介</span><span class="sxs-lookup"><span data-stu-id="47364-102">SYNOPSIS</span></span>
<span data-ttu-id="47364-103">此命令可讓使用者根據 VPN 閘道上預先設定 vpn 設定建立 Vpn 設定檔套件，以及使用者可能需要設定的其他設定，例如一些根憑證。</span><span class="sxs-lookup"><span data-stu-id="47364-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="47364-104">語法</span><span class="sxs-lookup"><span data-stu-id="47364-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47364-105">描述</span><span class="sxs-lookup"><span data-stu-id="47364-105">DESCRIPTION</span></span>
<span data-ttu-id="47364-106">這可讓使用者根據 VPN 閘道上預先設定 VPN 設定建立 Vpn 設定檔套件，以及一些使用者可能需要設定的其他設定，例如一些根憑證。</span><span class="sxs-lookup"><span data-stu-id="47364-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="47364-107">例子</span><span class="sxs-lookup"><span data-stu-id="47364-107">EXAMPLES</span></span>

### <span data-ttu-id="47364-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="47364-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="47364-109">此 Cmdlet 用於為 ResourceGroup "ContosoResourceGroup" 中的 "ContosoVirtualNetworkGateway" 建立 VPN 用戶端設定檔 zip 檔案。</span><span class="sxs-lookup"><span data-stu-id="47364-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="47364-110">設定檔的產生位置為預先配置的弧形伺服器，該伺服器已針對 VpnProfileRadiusCert 憑證檔案使用 "EAPTLS" 驗證方法。</span><span class="sxs-lookup"><span data-stu-id="47364-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="47364-111">參數</span><span class="sxs-lookup"><span data-stu-id="47364-111">PARAMETERS</span></span>

### <span data-ttu-id="47364-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="47364-112">-AuthenticationMethod</span></span>
<span data-ttu-id="47364-113">驗證方法可以取值 EAPMSCHAPv2 或 EAPTLS。</span><span class="sxs-lookup"><span data-stu-id="47364-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="47364-114">指定 EAPMSCHAPv2 時，Cmdlet 會針對使用驗證通訊協定的使用者名稱/密碼驗證產生EAP-MSCHAPv2安裝程式。</span><span class="sxs-lookup"><span data-stu-id="47364-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="47364-115">如果指定 EAPTLS，Cmdlet 會針對使用 EAP-TLS 通訊協定的憑證驗證產生用戶端組組安裝程式。</span><span class="sxs-lookup"><span data-stu-id="47364-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="47364-116">「EapTls」選項可用來上傳信任的根目錄，同時用於以 RADIUS 為基礎的憑證驗證，以及由虛擬網路閘道執行的認證驗證。</span><span class="sxs-lookup"><span data-stu-id="47364-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="47364-117">Cmdlet 會自動偵測到已配置哪些專案。</span><span class="sxs-lookup"><span data-stu-id="47364-117">The cmdlet automatically detects what is configured.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EAPTLS, EAPMSCHAPv2

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47364-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="47364-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="47364-119">用戶端根憑證路徑清單</span><span class="sxs-lookup"><span data-stu-id="47364-119">A list of client root certificate paths</span></span>

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

### <span data-ttu-id="47364-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47364-120">-DefaultProfile</span></span>
<span data-ttu-id="47364-121">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="47364-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47364-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="47364-122">-Name</span></span>
<span data-ttu-id="47364-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="47364-123">The resource name.</span></span>

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

### <span data-ttu-id="47364-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="47364-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="47364-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="47364-125">ProcessorArchitecture</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Amd64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47364-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="47364-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="47364-127">弧線伺服器根憑證路徑。</span><span class="sxs-lookup"><span data-stu-id="47364-127">Radius server root certificate path.</span></span> <span data-ttu-id="47364-128">這是使用具有 RADIUS 驗證的 EAP-TLS 時必須指定的強制參數。</span><span class="sxs-lookup"><span data-stu-id="47364-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="47364-129">這是 .cer 檔案的完整路徑名稱，其中包含在驗證期間用戶端用來驗證 RADIUS 伺服器之 RADIUS 根憑證。</span><span class="sxs-lookup"><span data-stu-id="47364-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47364-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47364-130">-ResourceGroupName</span></span>
<span data-ttu-id="47364-131">資源組名。</span><span class="sxs-lookup"><span data-stu-id="47364-131">The resource group name.</span></span>

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

### <span data-ttu-id="47364-132">-確認</span><span class="sxs-lookup"><span data-stu-id="47364-132">-Confirm</span></span>
<span data-ttu-id="47364-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="47364-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47364-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47364-134">-WhatIf</span></span>
<span data-ttu-id="47364-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="47364-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47364-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47364-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47364-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47364-137">CommonParameters</span></span>
<span data-ttu-id="47364-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="47364-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47364-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="47364-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47364-140">輸入</span><span class="sxs-lookup"><span data-stu-id="47364-140">INPUTS</span></span>

### <span data-ttu-id="47364-141">System.String</span><span class="sxs-lookup"><span data-stu-id="47364-141">System.String</span></span>

### <span data-ttu-id="47364-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="47364-142">System.String[]</span></span>

## <span data-ttu-id="47364-143">輸出</span><span class="sxs-lookup"><span data-stu-id="47364-143">OUTPUTS</span></span>

### <span data-ttu-id="47364-144">Microsoft.Azure.Commands.Network.models.PS VpnProfile</span><span class="sxs-lookup"><span data-stu-id="47364-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="47364-145">筆記</span><span class="sxs-lookup"><span data-stu-id="47364-145">NOTES</span></span>

## <span data-ttu-id="47364-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="47364-146">RELATED LINKS</span></span>

[<span data-ttu-id="47364-147">Get-Az VpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="47364-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
