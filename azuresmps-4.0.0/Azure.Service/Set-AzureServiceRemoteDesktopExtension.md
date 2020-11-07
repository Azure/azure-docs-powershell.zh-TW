---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967259"
---
# <span data-ttu-id="c291a-101">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="c291a-101">Set-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="c291a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c291a-102">SYNOPSIS</span></span>
<span data-ttu-id="c291a-103">在已部署服務或部署上的指定角色上啟用遠端桌面延伸 (s) 或所有角色。</span><span class="sxs-lookup"><span data-stu-id="c291a-103">Enables remote desktop extension on specified role(s) or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="c291a-104">句法</span><span class="sxs-lookup"><span data-stu-id="c291a-104">SYNTAX</span></span>

### <span data-ttu-id="c291a-105">SetExtension (預設) </span><span class="sxs-lookup"><span data-stu-id="c291a-105">SetExtension (Default)</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c291a-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="c291a-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c291a-107">說明</span><span class="sxs-lookup"><span data-stu-id="c291a-107">DESCRIPTION</span></span>
<span data-ttu-id="c291a-108">**AzureServiceRemoteDesktopExtension** Cmdlet 可在已部署服務或部署上的指定角色或所有角色上啟用遠端桌面延伸。</span><span class="sxs-lookup"><span data-stu-id="c291a-108">The **Set-AzureServiceRemoteDesktopExtension** cmdlet enables remote desktop extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="c291a-109">示例</span><span class="sxs-lookup"><span data-stu-id="c291a-109">EXAMPLES</span></span>

### <span data-ttu-id="c291a-110">範例1：啟用遠端桌面延伸</span><span class="sxs-lookup"><span data-stu-id="c291a-110">Example 1: Enable remote desktop extension</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

<span data-ttu-id="c291a-111">這個命令可為指定的服務啟用遠端桌面延伸。</span><span class="sxs-lookup"><span data-stu-id="c291a-111">This command enables the remote desktop extension for the specified service.</span></span>

### <span data-ttu-id="c291a-112">範例2：針對指定的角色啟用遠端桌面延伸</span><span class="sxs-lookup"><span data-stu-id="c291a-112">Example 2: Enable remote desktop extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

<span data-ttu-id="c291a-113">這個命令可為指定的服務和角色啟用遠端桌面延伸。</span><span class="sxs-lookup"><span data-stu-id="c291a-113">This command enables the remote desktop extension for the specified service and role.</span></span>

## <span data-ttu-id="c291a-114">參數</span><span class="sxs-lookup"><span data-stu-id="c291a-114">PARAMETERS</span></span>

### <span data-ttu-id="c291a-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="c291a-115">-CertificateThumbprint</span></span>
<span data-ttu-id="c291a-116">指定要用來加密私人配置的憑證指紋。</span><span class="sxs-lookup"><span data-stu-id="c291a-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="c291a-117">此憑證必須已存在於憑證存放區中。</span><span class="sxs-lookup"><span data-stu-id="c291a-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="c291a-118">如果您沒有指定憑證，此 Cmdlet 會建立證書。</span><span class="sxs-lookup"><span data-stu-id="c291a-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-119">-認證</span><span class="sxs-lookup"><span data-stu-id="c291a-119">-Credential</span></span>
<span data-ttu-id="c291a-120">指定要為遠端桌面啟用的認證。</span><span class="sxs-lookup"><span data-stu-id="c291a-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="c291a-121">認證包括使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="c291a-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-122">-到期日</span><span class="sxs-lookup"><span data-stu-id="c291a-122">-Expiration</span></span>
<span data-ttu-id="c291a-123">指定 [日期時間] 物件，讓使用者指定使用者帳戶到期的時間。</span><span class="sxs-lookup"><span data-stu-id="c291a-123">Specifies a date time object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="c291a-124">-ExtensionId</span></span>
<span data-ttu-id="c291a-125">指定延伸 ID。</span><span class="sxs-lookup"><span data-stu-id="c291a-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c291a-126">-InformationAction</span></span>
<span data-ttu-id="c291a-127">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="c291a-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c291a-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="c291a-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c291a-129">持續</span><span class="sxs-lookup"><span data-stu-id="c291a-129">Continue</span></span>
- <span data-ttu-id="c291a-130">理會</span><span class="sxs-lookup"><span data-stu-id="c291a-130">Ignore</span></span>
- <span data-ttu-id="c291a-131">看</span><span class="sxs-lookup"><span data-stu-id="c291a-131">Inquire</span></span>
- <span data-ttu-id="c291a-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c291a-132">SilentlyContinue</span></span>
- <span data-ttu-id="c291a-133">停止</span><span class="sxs-lookup"><span data-stu-id="c291a-133">Stop</span></span>
- <span data-ttu-id="c291a-134">封存</span><span class="sxs-lookup"><span data-stu-id="c291a-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c291a-135">-InformationVariable</span></span>
<span data-ttu-id="c291a-136">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="c291a-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-137">-設定檔</span><span class="sxs-lookup"><span data-stu-id="c291a-137">-Profile</span></span>
<span data-ttu-id="c291a-138">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="c291a-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c291a-139">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="c291a-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-140">-角色</span><span class="sxs-lookup"><span data-stu-id="c291a-140">-Role</span></span>
<span data-ttu-id="c291a-141">指定要指定其遠端桌面設定的選擇性角色陣列。</span><span class="sxs-lookup"><span data-stu-id="c291a-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="c291a-142">如果未指定此參數，則會將遠端桌面設定套用為所有角色的預設配置。</span><span class="sxs-lookup"><span data-stu-id="c291a-142">If this parameter is not specified, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c291a-143">-ServiceName</span></span>
<span data-ttu-id="c291a-144">指定部署的 Azure 服務名稱。</span><span class="sxs-lookup"><span data-stu-id="c291a-144">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-145">-槽</span><span class="sxs-lookup"><span data-stu-id="c291a-145">-Slot</span></span>
<span data-ttu-id="c291a-146">指定要修改的部署環境。</span><span class="sxs-lookup"><span data-stu-id="c291a-146">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="c291a-147">此參數可接受的值為： [生產]、[轉移]。</span><span class="sxs-lookup"><span data-stu-id="c291a-147">The acceptable values for this parameter are: Production, Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-148">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c291a-148">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="c291a-149">指定與指紋搭配使用以識別憑證的指紋雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="c291a-149">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="c291a-150">這個參數是選用的，預設值是 sha1。</span><span class="sxs-lookup"><span data-stu-id="c291a-150">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-151">-版本</span><span class="sxs-lookup"><span data-stu-id="c291a-151">-Version</span></span>
<span data-ttu-id="c291a-152">指定副檔名版本。</span><span class="sxs-lookup"><span data-stu-id="c291a-152">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-153">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="c291a-153">-X509Certificate</span></span>
<span data-ttu-id="c291a-154">指定會自動上傳到雲端服務並用來加密延伸私人配置的 x509 憑證。</span><span class="sxs-lookup"><span data-stu-id="c291a-154">Specifies an x509 certificate that is automatically uploaded to the cloud service and used for encrypting the private configuration of the extension.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c291a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c291a-155">CommonParameters</span></span>
<span data-ttu-id="c291a-156">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c291a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c291a-157">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c291a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c291a-158">輸入</span><span class="sxs-lookup"><span data-stu-id="c291a-158">INPUTS</span></span>

## <span data-ttu-id="c291a-159">輸出</span><span class="sxs-lookup"><span data-stu-id="c291a-159">OUTPUTS</span></span>

## <span data-ttu-id="c291a-160">筆記</span><span class="sxs-lookup"><span data-stu-id="c291a-160">NOTES</span></span>

## <span data-ttu-id="c291a-161">相關連結</span><span class="sxs-lookup"><span data-stu-id="c291a-161">RELATED LINKS</span></span>

[<span data-ttu-id="c291a-162">AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="c291a-162">Get-AzureServiceRemoteDesktopExtension</span></span>](./Get-AzureServiceRemoteDesktopExtension.md)


