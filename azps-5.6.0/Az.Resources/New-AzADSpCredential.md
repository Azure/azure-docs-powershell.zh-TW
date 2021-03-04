---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 38952cb7c7deebb76568bef2a2062d20c3c1b497
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907086"
---
# <span data-ttu-id="5d144-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5d144-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="5d144-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5d144-102">SYNOPSIS</span></span>
<span data-ttu-id="5d144-103">新增認證至現有的服務主體。</span><span class="sxs-lookup"><span data-stu-id="5d144-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="5d144-104">語法</span><span class="sxs-lookup"><span data-stu-id="5d144-104">SYNTAX</span></span>

### <span data-ttu-id="5d144-105">SpObjectIdWithPasswordParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5d144-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d144-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d144-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d144-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d144-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d144-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d144-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d144-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d144-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d144-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d144-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d144-111">描述</span><span class="sxs-lookup"><span data-stu-id="5d144-111">DESCRIPTION</span></span>
<span data-ttu-id="5d144-112">您可以使用 New-AzADSpCredential Cmdlet 來新增認證或匯總服務主體的認證。</span><span class="sxs-lookup"><span data-stu-id="5d144-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="5d144-113">服務主體是提供物件識別碼或服務主體名稱來識別。</span><span class="sxs-lookup"><span data-stu-id="5d144-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="5d144-114">例子</span><span class="sxs-lookup"><span data-stu-id="5d144-114">EXAMPLES</span></span>

### <span data-ttu-id="5d144-115">範例 1：使用產生的密碼建立新服務主體認證</span><span class="sxs-lookup"><span data-stu-id="5d144-115">Example 1: Create a new service principal credential using a generated password</span></span>

```powershell
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="5d144-116">新的密碼認證會新增到現有服務主體，物件識別碼為 '1f99cf81-0146-4f4e-beae-2007d0668476'。</span><span class="sxs-lookup"><span data-stu-id="5d144-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="5d144-117">範例 2：使用憑證建立新服務主體認證</span><span class="sxs-lookup"><span data-stu-id="5d144-117">Example 2: Create a new service principal credential using a certificate</span></span>

```powershell
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="5d144-118">提供的 base64 編碼公用 X509 憑證 ("myapp.cer") 會使用 SPN 新增到現有的服務主體。</span><span class="sxs-lookup"><span data-stu-id="5d144-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="5d144-119">範例 3：使用管道建立新服務主體認證</span><span class="sxs-lookup"><span data-stu-id="5d144-119">Example 3: Create a new service principal credential using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="5d144-120">使用物件識別碼 '1f99cf81-0146-4f4e-beae-2007d0668476' 和服務管道到 New-AzADSpCredential，以產生密碼為該服務主體建立新服務主體認證的服務主體。</span><span class="sxs-lookup"><span data-stu-id="5d144-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="5d144-121">參數</span><span class="sxs-lookup"><span data-stu-id="5d144-121">PARAMETERS</span></span>

### <span data-ttu-id="5d144-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="5d144-122">-CertValue</span></span>
<span data-ttu-id="5d144-123">「非對稱」認證類型的值。</span><span class="sxs-lookup"><span data-stu-id="5d144-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="5d144-124">它代表基礎 64 編碼憑證。</span><span class="sxs-lookup"><span data-stu-id="5d144-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="5d144-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d144-125">-DefaultProfile</span></span>
<span data-ttu-id="5d144-126">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="5d144-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d144-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="5d144-127">-EndDate</span></span>
<span data-ttu-id="5d144-128">認證使用量的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="5d144-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="5d144-129">預設結束日期為自今天起一年。</span><span class="sxs-lookup"><span data-stu-id="5d144-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="5d144-130">對於「非對稱」類型認證，這必須設定為 X509 憑證有效日期當天或之前。</span><span class="sxs-lookup"><span data-stu-id="5d144-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="5d144-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5d144-131">-ObjectId</span></span>
<span data-ttu-id="5d144-132">要新增認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d144-132">The object id of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="5d144-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5d144-133">-ServicePrincipalName</span></span>
<span data-ttu-id="5d144-134">SPN (名稱) 要新增認證之服務主體的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d144-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="5d144-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="5d144-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="5d144-136">要新增認證的服務主體物件。</span><span class="sxs-lookup"><span data-stu-id="5d144-136">The service principal object to add the credentials to.</span></span>

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

### <span data-ttu-id="5d144-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="5d144-137">-StartDate</span></span>
<span data-ttu-id="5d144-138">認證使用量的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="5d144-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="5d144-139">預設的開始日期值是今天。</span><span class="sxs-lookup"><span data-stu-id="5d144-139">The default start date value is today.</span></span>
<span data-ttu-id="5d144-140">對於「非對稱」類型認證，這必須設定為 X509 憑證的有效日期當天或之後。</span><span class="sxs-lookup"><span data-stu-id="5d144-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="5d144-141">-確認</span><span class="sxs-lookup"><span data-stu-id="5d144-141">-Confirm</span></span>
<span data-ttu-id="5d144-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5d144-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d144-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d144-143">-WhatIf</span></span>
<span data-ttu-id="5d144-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5d144-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d144-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d144-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d144-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d144-146">CommonParameters</span></span>
<span data-ttu-id="5d144-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5d144-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d144-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d144-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d144-149">輸入</span><span class="sxs-lookup"><span data-stu-id="5d144-149">INPUTS</span></span>

### <span data-ttu-id="5d144-150">System.String</span><span class="sxs-lookup"><span data-stu-id="5d144-150">System.String</span></span>

### <span data-ttu-id="5d144-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d144-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="5d144-152">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="5d144-152">System.DateTime</span></span>

## <span data-ttu-id="5d144-153">輸出</span><span class="sxs-lookup"><span data-stu-id="5d144-153">OUTPUTS</span></span>

### <span data-ttu-id="5d144-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="5d144-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="5d144-155">Microsoft.Azure.Commands.Resources.models.Authorization.PSADCredential方apper</span><span class="sxs-lookup"><span data-stu-id="5d144-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="5d144-156">筆記</span><span class="sxs-lookup"><span data-stu-id="5d144-156">NOTES</span></span>

## <span data-ttu-id="5d144-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d144-157">RELATED LINKS</span></span>

[<span data-ttu-id="5d144-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5d144-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="5d144-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5d144-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="5d144-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d144-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



