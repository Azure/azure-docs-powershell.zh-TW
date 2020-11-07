---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 98f127386a606881a0f8359e605ee2b96168a9b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93798326"
---
# <span data-ttu-id="8c3f3-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8c3f3-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="8c3f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8c3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="8c3f3-103">將認證新增至現有的服務主體。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="8c3f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="8c3f3-104">SYNTAX</span></span>

### <span data-ttu-id="8c3f3-105">SpObjectIdWithPasswordParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8c3f3-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3f3-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c3f3-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3f3-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c3f3-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3f3-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c3f3-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3f3-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c3f3-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8c3f3-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="8c3f3-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c3f3-111">說明</span><span class="sxs-lookup"><span data-stu-id="8c3f3-111">DESCRIPTION</span></span>
<span data-ttu-id="8c3f3-112">New-AzADSpCredential Cmdlet 可以用來新增認證，或為服務主體轉移認證。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="8c3f3-113">服務主體是透過提供物件識別碼或服務主體名稱來識別。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="8c3f3-114">示例</span><span class="sxs-lookup"><span data-stu-id="8c3f3-114">EXAMPLES</span></span>

### <span data-ttu-id="8c3f3-115">範例 1-使用產生的密碼建立新的服務主體認證</span><span class="sxs-lookup"><span data-stu-id="8c3f3-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="8c3f3-116">新的密碼認證會新增至現有的服務主體，物件 id 為 ' 1f99cf81-0146-4f4e-beae-2007d0668476」。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="8c3f3-117">範例 2-使用憑證建立新的服務主體認證</span><span class="sxs-lookup"><span data-stu-id="8c3f3-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="8c3f3-118">提供的 base64 編碼公用 X509 憑證 ( "myapp" ) 是使用其 SPN 新增至現有的服務主體。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="8c3f3-119">範例 3-使用管道建立新的服務主體認證</span><span class="sxs-lookup"><span data-stu-id="8c3f3-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="8c3f3-120">取得1f99cf81-0146-4f4e-beae-2007d0668476 的服務主體，以及 New-AzADSpCredential 的管道，以使用產生的密碼為該服務主體建立新的服務主體認證。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="8c3f3-121">參數</span><span class="sxs-lookup"><span data-stu-id="8c3f3-121">PARAMETERS</span></span>

### <span data-ttu-id="8c3f3-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="8c3f3-122">-CertValue</span></span>
<span data-ttu-id="8c3f3-123">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="8c3f3-124">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3f3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c3f3-125">-DefaultProfile</span></span>
<span data-ttu-id="8c3f3-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8c3f3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c3f3-127">-結束日期</span><span class="sxs-lookup"><span data-stu-id="8c3f3-127">-EndDate</span></span>
<span data-ttu-id="8c3f3-128">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="8c3f3-129">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="8c3f3-130">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3f3-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8c3f3-131">-ObjectId</span></span>
<span data-ttu-id="8c3f3-132">要新增認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3f3-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="8c3f3-133">-ServicePrincipalName</span></span>
<span data-ttu-id="8c3f3-134">要新增認證之服務主體 (SPN) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-134">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3f3-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="8c3f3-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="8c3f3-136">要新增認證的服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-136">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3f3-137">-開始日期</span><span class="sxs-lookup"><span data-stu-id="8c3f3-137">-StartDate</span></span>
<span data-ttu-id="8c3f3-138">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="8c3f3-139">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-139">The default start date value is today.</span></span>
<span data-ttu-id="8c3f3-140">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c3f3-141">-確認</span><span class="sxs-lookup"><span data-stu-id="8c3f3-141">-Confirm</span></span>
<span data-ttu-id="8c3f3-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c3f3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c3f3-143">-WhatIf</span></span>
<span data-ttu-id="8c3f3-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c3f3-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c3f3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c3f3-146">CommonParameters</span></span>
<span data-ttu-id="8c3f3-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c3f3-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c3f3-149">輸入</span><span class="sxs-lookup"><span data-stu-id="8c3f3-149">INPUTS</span></span>

### <span data-ttu-id="8c3f3-150">System.object</span><span class="sxs-lookup"><span data-stu-id="8c3f3-150">System.String</span></span>

### <span data-ttu-id="8c3f3-151">PSADServicePrincipal （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="8c3f3-152">System.object</span><span class="sxs-lookup"><span data-stu-id="8c3f3-152">System.DateTime</span></span>

## <span data-ttu-id="8c3f3-153">輸出</span><span class="sxs-lookup"><span data-stu-id="8c3f3-153">OUTPUTS</span></span>

### <span data-ttu-id="8c3f3-154">PSADCredential （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="8c3f3-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="8c3f3-155">PSADCredentialWrapper 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="8c3f3-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="8c3f3-156">筆記</span><span class="sxs-lookup"><span data-stu-id="8c3f3-156">NOTES</span></span>

## <span data-ttu-id="8c3f3-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="8c3f3-157">RELATED LINKS</span></span>

[<span data-ttu-id="8c3f3-158">AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8c3f3-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="8c3f3-159">移除-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="8c3f3-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="8c3f3-160">AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8c3f3-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



