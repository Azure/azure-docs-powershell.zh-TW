---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientConfiguration.md
ms.openlocfilehash: 11b18f0a0f12a82e88694fd91ce89956951a4eb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100133831"
---
# <span data-ttu-id="e385c-101">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e385c-101">New-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="e385c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e385c-102">SYNOPSIS</span></span>
<span data-ttu-id="e385c-103">這個命令可讓使用者根據 VPN 閘道預先設定的 Vpn 設定來建立 Vpn 設定檔套件，除了其他使用者可能需要設定的設定（例如，某些根憑證）。</span><span class="sxs-lookup"><span data-stu-id="e385c-103">This command allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="e385c-104">句法</span><span class="sxs-lookup"><span data-stu-id="e385c-104">SYNTAX</span></span>

```
New-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String> [-ProcessorArchitecture <String>]
 [-AuthenticationMethod <String>] [-RadiusRootCertificateFile <String>]
 [-ClientRootCertificateFileList <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e385c-105">說明</span><span class="sxs-lookup"><span data-stu-id="e385c-105">DESCRIPTION</span></span>
<span data-ttu-id="e385c-106">這可讓使用者根據 VPN 閘道預先設定的 Vpn 設定，以及其他使用者可能需要設定的其他設定（例如，某些根憑證）來建立 Vpn 設定檔套件。</span><span class="sxs-lookup"><span data-stu-id="e385c-106">this allows the users to create the Vpn profile package based on pre-configured vpn settings on the VPN gateway, in addition to some additional settings that users may need to configure, for e.g. some root certificates.</span></span>

## <span data-ttu-id="e385c-107">示例</span><span class="sxs-lookup"><span data-stu-id="e385c-107">EXAMPLES</span></span>

### <span data-ttu-id="e385c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e385c-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -ResourceGroupName "ContosoResourceGroup" -Name "ContosoVirtualNetworkGateway" -AuthenticationMethod "EAPTLS" -RadiusRootCertificateFile "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"
```

<span data-ttu-id="e385c-109">這個 Cmdlet 是用來針對 ResourceGroup "ContosoResourceGroup" 中的 "ContosoVirtualNetworkGateway" 建立 VPN 用戶端設定檔 zip 檔案。</span><span class="sxs-lookup"><span data-stu-id="e385c-109">This cmdlet is used to create a VPN client profile zip file for "ContosoVirtualNetworkGateway" in ResourceGroup "ContosoResourceGroup".</span></span> <span data-ttu-id="e385c-110">設定檔是針對預先設定的 radius 伺服器所產生，設定為將 "EAPTLS" 驗證方法與 VpnProfileRadiusCert 憑證檔案搭配使用。</span><span class="sxs-lookup"><span data-stu-id="e385c-110">The profile is generated for a pre-configured radius server that is configured to use "EAPTLS" authentication method with the VpnProfileRadiusCert certificate file.</span></span>

## <span data-ttu-id="e385c-111">參數</span><span class="sxs-lookup"><span data-stu-id="e385c-111">PARAMETERS</span></span>

### <span data-ttu-id="e385c-112">-AuthenticationMethod</span><span class="sxs-lookup"><span data-stu-id="e385c-112">-AuthenticationMethod</span></span>
<span data-ttu-id="e385c-113">驗證方法可以採用值 EAPMSCHAPv2 或 EAPTLS。</span><span class="sxs-lookup"><span data-stu-id="e385c-113">Authentication Method Can take values EAPMSCHAPv2 or EAPTLS.</span></span> <span data-ttu-id="e385c-114">指定 EAPMSCHAPv2 之後，Cmdlet 會針對使用 EAP-MSCHAPv2 驗證通訊協定的使用者名稱/密碼驗證產生用戶端配置安裝程式。</span><span class="sxs-lookup"><span data-stu-id="e385c-114">When EAPMSCHAPv2 is specified then the cmdlet generates a client configuration installer for username/password authentication that uses EAP-MSCHAPv2 authentication protocol.</span></span> <span data-ttu-id="e385c-115">如果已指定 EAPTLS，則 Cmdlet 會針對使用 EAP-TLS 通訊協定的憑證驗證產生用戶端配置安裝程式。</span><span class="sxs-lookup"><span data-stu-id="e385c-115">If EAPTLS is specified then the cmdlet generates a client configuration installer for certificate authentication that uses EAP-TLS protocol.</span></span> <span data-ttu-id="e385c-116">"EapTls" 選項可用於以 RADIUS 為基礎的憑證驗證，以及由虛擬網路閘道上傳受信任的根所執行的認證驗證。</span><span class="sxs-lookup"><span data-stu-id="e385c-116">The "EapTls" option can be used for both RADIUS-based certificate authentication and certification authentication performed by the Virtual Network Gateway by uploading the trusted root.</span></span> <span data-ttu-id="e385c-117">這個 Cmdlet 會自動偵測已設定的內容。</span><span class="sxs-lookup"><span data-stu-id="e385c-117">The cmdlet automatically detects what is configured.</span></span>

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

### <span data-ttu-id="e385c-118">-ClientRootCertificateFileList</span><span class="sxs-lookup"><span data-stu-id="e385c-118">-ClientRootCertificateFileList</span></span>
<span data-ttu-id="e385c-119">用戶端根憑證路徑清單</span><span class="sxs-lookup"><span data-stu-id="e385c-119">A list of client root certificate paths</span></span>

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

### <span data-ttu-id="e385c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e385c-120">-DefaultProfile</span></span>
<span data-ttu-id="e385c-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e385c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e385c-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="e385c-122">-Name</span></span>
<span data-ttu-id="e385c-123">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="e385c-123">The resource name.</span></span>

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

### <span data-ttu-id="e385c-124">-ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="e385c-124">-ProcessorArchitecture</span></span>
<span data-ttu-id="e385c-125">ProcessorArchitecture</span><span class="sxs-lookup"><span data-stu-id="e385c-125">ProcessorArchitecture</span></span>

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

### <span data-ttu-id="e385c-126">-RadiusRootCertificateFile</span><span class="sxs-lookup"><span data-stu-id="e385c-126">-RadiusRootCertificateFile</span></span>
<span data-ttu-id="e385c-127">Radius 伺服器根憑證路徑。</span><span class="sxs-lookup"><span data-stu-id="e385c-127">Radius server root certificate path.</span></span> <span data-ttu-id="e385c-128">這個強制性參數必須在使用 RADIUS 驗證的 EAP TLS 時指定。</span><span class="sxs-lookup"><span data-stu-id="e385c-128">This is a mandatory parameter that has to be specified when EAP-TLS with RADIUS authentication is used.</span></span> <span data-ttu-id="e385c-129">這是 .cer 檔案的完整路徑名稱，其中包含用戶端用來驗證 RADIUS 伺服器在驗證期間的 RADIUS 根憑證。</span><span class="sxs-lookup"><span data-stu-id="e385c-129">This is the full path name of .cer file containing the RADIUS root certificate that the client uses to validates the RADIUS server during authentication.</span></span>

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

### <span data-ttu-id="e385c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e385c-130">-ResourceGroupName</span></span>
<span data-ttu-id="e385c-131">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e385c-131">The resource group name.</span></span>

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

### <span data-ttu-id="e385c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="e385c-132">-Confirm</span></span>
<span data-ttu-id="e385c-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e385c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e385c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e385c-134">-WhatIf</span></span>
<span data-ttu-id="e385c-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e385c-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e385c-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e385c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e385c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e385c-137">CommonParameters</span></span>
<span data-ttu-id="e385c-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e385c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e385c-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e385c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e385c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="e385c-140">INPUTS</span></span>

### <span data-ttu-id="e385c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="e385c-141">System.String</span></span>

### <span data-ttu-id="e385c-142">System.object []</span><span class="sxs-lookup"><span data-stu-id="e385c-142">System.String[]</span></span>

## <span data-ttu-id="e385c-143">輸出</span><span class="sxs-lookup"><span data-stu-id="e385c-143">OUTPUTS</span></span>

### <span data-ttu-id="e385c-144">PSVpnProfile 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="e385c-144">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="e385c-145">筆記</span><span class="sxs-lookup"><span data-stu-id="e385c-145">NOTES</span></span>

## <span data-ttu-id="e385c-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="e385c-146">RELATED LINKS</span></span>

[<span data-ttu-id="e385c-147">AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="e385c-147">Get-AzVpnClientConfiguration</span></span>](./Get-AzVpnClientConfiguration.md)
