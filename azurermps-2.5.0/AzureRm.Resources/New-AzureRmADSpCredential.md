---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: 2f4a5e19f9b563361b526fab386c068fe65ce6ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801937"
---
# <span data-ttu-id="1cf75-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1cf75-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="1cf75-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1cf75-102">SYNOPSIS</span></span>
<span data-ttu-id="1cf75-103">將認證新增至現有的服務主體。</span><span class="sxs-lookup"><span data-stu-id="1cf75-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cf75-104">句法</span><span class="sxs-lookup"><span data-stu-id="1cf75-104">SYNTAX</span></span>

### <span data-ttu-id="1cf75-105">SpObjectIdWithPasswordParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="1cf75-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <Guid> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf75-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cf75-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf75-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cf75-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf75-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cf75-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cf75-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cf75-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1cf75-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="1cf75-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1cf75-111">說明</span><span class="sxs-lookup"><span data-stu-id="1cf75-111">DESCRIPTION</span></span>
<span data-ttu-id="1cf75-112">New-AzureRmADSpCredential Cmdlet 可以用來新增認證，或為服務主體轉移認證。</span><span class="sxs-lookup"><span data-stu-id="1cf75-112">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="1cf75-113">服務主體是透過提供物件識別碼或服務主體名稱來識別。</span><span class="sxs-lookup"><span data-stu-id="1cf75-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="1cf75-114">示例</span><span class="sxs-lookup"><span data-stu-id="1cf75-114">EXAMPLES</span></span>

### <span data-ttu-id="1cf75-115">範例 1-使用產生的密碼建立新的服務主體認證</span><span class="sxs-lookup"><span data-stu-id="1cf75-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="1cf75-116">新的密碼認證會新增至現有的服務主體，物件 id 為 ' 1f99cf81-0146-4f4e-beae-2007d0668476」。</span><span class="sxs-lookup"><span data-stu-id="1cf75-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="1cf75-117">範例 2-使用憑證建立新的服務主體認證</span><span class="sxs-lookup"><span data-stu-id="1cf75-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="1cf75-118">提供的 base64 編碼公用 X509 憑證 ( "myapp" ) 是使用其 SPN 新增至現有的服務主體。</span><span class="sxs-lookup"><span data-stu-id="1cf75-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="1cf75-119">範例 3-使用管道建立新的服務主體認證</span><span class="sxs-lookup"><span data-stu-id="1cf75-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzureRmADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="1cf75-120">取得1f99cf81-0146-4f4e-beae-2007d0668476 的服務主體，以及 New-AzureRmADSpCredential 的管道，以使用產生的密碼為該服務主體建立新的服務主體認證。</span><span class="sxs-lookup"><span data-stu-id="1cf75-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzureRmADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="1cf75-121">參數</span><span class="sxs-lookup"><span data-stu-id="1cf75-121">PARAMETERS</span></span>

### <span data-ttu-id="1cf75-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="1cf75-122">-CertValue</span></span>
<span data-ttu-id="1cf75-123">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="1cf75-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="1cf75-124">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="1cf75-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="1cf75-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cf75-125">-DefaultProfile</span></span>
<span data-ttu-id="1cf75-126">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1cf75-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1cf75-127">-結束日期</span><span class="sxs-lookup"><span data-stu-id="1cf75-127">-EndDate</span></span>
<span data-ttu-id="1cf75-128">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="1cf75-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="1cf75-129">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="1cf75-129">The default end date value is one year from today.</span></span> <span data-ttu-id="1cf75-130">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="1cf75-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="1cf75-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1cf75-131">-ObjectId</span></span>
<span data-ttu-id="1cf75-132">要新增認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="1cf75-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf75-133">-Password</span><span class="sxs-lookup"><span data-stu-id="1cf75-133">-Password</span></span>
<span data-ttu-id="1cf75-134">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="1cf75-134">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf75-135">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="1cf75-135">-ServicePrincipalName</span></span>
<span data-ttu-id="1cf75-136">要新增認證之服務主體 (SPN) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="1cf75-136">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="1cf75-137">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="1cf75-137">-ServicePrincipalObject</span></span>
<span data-ttu-id="1cf75-138">要新增認證的服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="1cf75-138">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cf75-139">-開始日期</span><span class="sxs-lookup"><span data-stu-id="1cf75-139">-StartDate</span></span>
<span data-ttu-id="1cf75-140">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="1cf75-140">The effective start date of the credential usage.</span></span>
<span data-ttu-id="1cf75-141">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="1cf75-141">The default start date value is today.</span></span> <span data-ttu-id="1cf75-142">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="1cf75-142">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="1cf75-143">-確認</span><span class="sxs-lookup"><span data-stu-id="1cf75-143">-Confirm</span></span>
<span data-ttu-id="1cf75-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1cf75-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cf75-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cf75-145">-WhatIf</span></span>
<span data-ttu-id="1cf75-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1cf75-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cf75-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1cf75-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cf75-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cf75-148">CommonParameters</span></span>
<span data-ttu-id="1cf75-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1cf75-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cf75-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1cf75-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cf75-151">輸入</span><span class="sxs-lookup"><span data-stu-id="1cf75-151">INPUTS</span></span>

### <span data-ttu-id="1cf75-152">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="1cf75-152">System.Guid</span></span>

### <span data-ttu-id="1cf75-153">System.object</span><span class="sxs-lookup"><span data-stu-id="1cf75-153">System.String</span></span>

### <span data-ttu-id="1cf75-154">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1cf75-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="1cf75-155">參數： ServicePrincipalObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="1cf75-155">Parameters: ServicePrincipalObject (ByValue)</span></span>

### <span data-ttu-id="1cf75-156">SecureString</span><span class="sxs-lookup"><span data-stu-id="1cf75-156">System.Security.SecureString</span></span>

### <span data-ttu-id="1cf75-157">System.object</span><span class="sxs-lookup"><span data-stu-id="1cf75-157">System.DateTime</span></span>

## <span data-ttu-id="1cf75-158">輸出</span><span class="sxs-lookup"><span data-stu-id="1cf75-158">OUTPUTS</span></span>

### <span data-ttu-id="1cf75-159">Microsoft.Azure.Graph.RBAC.Version1_6 PSADCredential</span><span class="sxs-lookup"><span data-stu-id="1cf75-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="1cf75-160">PSADCredentialWrapper 中的 [.Resources.]</span><span class="sxs-lookup"><span data-stu-id="1cf75-160">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="1cf75-161">筆記</span><span class="sxs-lookup"><span data-stu-id="1cf75-161">NOTES</span></span>

## <span data-ttu-id="1cf75-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="1cf75-162">RELATED LINKS</span></span>

[<span data-ttu-id="1cf75-163">AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1cf75-163">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="1cf75-164">移除-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="1cf75-164">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="1cf75-165">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1cf75-165">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



