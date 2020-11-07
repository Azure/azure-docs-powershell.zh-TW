---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: e0d842e1cd93932b92eff82d2c60dc228817b0e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93791238"
---
# <span data-ttu-id="bc466-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bc466-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="bc466-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bc466-102">SYNOPSIS</span></span>
<span data-ttu-id="bc466-103">在現有的應用程式中新增認證。</span><span class="sxs-lookup"><span data-stu-id="bc466-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="bc466-104">句法</span><span class="sxs-lookup"><span data-stu-id="bc466-104">SYNTAX</span></span>

### <span data-ttu-id="bc466-105">ApplicationObjectIdWithPasswordParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bc466-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc466-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc466-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc466-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc466-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc466-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc466-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc466-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc466-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc466-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc466-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc466-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc466-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc466-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="bc466-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bc466-113">說明</span><span class="sxs-lookup"><span data-stu-id="bc466-113">DESCRIPTION</span></span>
<span data-ttu-id="bc466-114">New-AzADAppCredential Cmdlet 可以用來新增認證或為應用程式轉移認證。</span><span class="sxs-lookup"><span data-stu-id="bc466-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="bc466-115">應用程式是透過提供應用程式物件識別碼或應用程式識別碼來識別。</span><span class="sxs-lookup"><span data-stu-id="bc466-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="bc466-116">示例</span><span class="sxs-lookup"><span data-stu-id="bc466-116">EXAMPLES</span></span>

### <span data-ttu-id="bc466-117">範例 1-使用密碼建立新的應用程式認證</span><span class="sxs-lookup"><span data-stu-id="bc466-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="bc466-118">新的密碼認證會新增至現有的應用程式，物件 id 為 ' 1f89cf81-0146-4f4e-beae-2007d0668416」。</span><span class="sxs-lookup"><span data-stu-id="bc466-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="bc466-119">範例 2-使用憑證建立新的應用程式認證</span><span class="sxs-lookup"><span data-stu-id="bc466-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="bc466-120">提供的 base64 編碼公用 X509 憑證 ( "myapp" ) 會新增至現有的應用程式，且有應用程式 id ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58」。</span><span class="sxs-lookup"><span data-stu-id="bc466-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="bc466-121">範例 3-使用管道建立新的應用程式認證</span><span class="sxs-lookup"><span data-stu-id="bc466-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="bc466-122">取得物件 id 為「1f89cf81-0146-4f4e-beae-2007d0668416」的應用程式，以及 New-AzADAppCredential 的管道，以使用指定的密碼為該應用程式建立新的應用程式認證。</span><span class="sxs-lookup"><span data-stu-id="bc466-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="bc466-123">參數</span><span class="sxs-lookup"><span data-stu-id="bc466-123">PARAMETERS</span></span>

### <span data-ttu-id="bc466-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bc466-124">-ApplicationId</span></span>
<span data-ttu-id="bc466-125">要新增認證之應用程式的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc466-125">The application id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc466-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="bc466-126">-ApplicationObject</span></span>
<span data-ttu-id="bc466-127">要新增認證的應用程式物件。</span><span class="sxs-lookup"><span data-stu-id="bc466-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc466-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="bc466-128">-CertValue</span></span>
<span data-ttu-id="bc466-129">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="bc466-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="bc466-130">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="bc466-130">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithCertValueParameterSet, ApplicationObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc466-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc466-131">-DefaultProfile</span></span>
<span data-ttu-id="bc466-132">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="bc466-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bc466-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bc466-133">-DisplayName</span></span>
<span data-ttu-id="bc466-134">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="bc466-134">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithPasswordParameterSet, DisplayNameWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc466-135">-結束日期</span><span class="sxs-lookup"><span data-stu-id="bc466-135">-EndDate</span></span>
<span data-ttu-id="bc466-136">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="bc466-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="bc466-137">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="bc466-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="bc466-138">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="bc466-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="bc466-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bc466-139">-ObjectId</span></span>
<span data-ttu-id="bc466-140">要新增認證之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc466-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc466-141">-Password</span><span class="sxs-lookup"><span data-stu-id="bc466-141">-Password</span></span>
<span data-ttu-id="bc466-142">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="bc466-142">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: DisplayNameWithPasswordParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc466-143">-開始日期</span><span class="sxs-lookup"><span data-stu-id="bc466-143">-StartDate</span></span>
<span data-ttu-id="bc466-144">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="bc466-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="bc466-145">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="bc466-145">The default start date value is today.</span></span> <span data-ttu-id="bc466-146">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="bc466-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="bc466-147">-確認</span><span class="sxs-lookup"><span data-stu-id="bc466-147">-Confirm</span></span>
<span data-ttu-id="bc466-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bc466-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc466-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc466-149">-WhatIf</span></span>
<span data-ttu-id="bc466-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bc466-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc466-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bc466-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc466-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc466-152">CommonParameters</span></span>
<span data-ttu-id="bc466-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bc466-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc466-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bc466-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc466-155">輸入</span><span class="sxs-lookup"><span data-stu-id="bc466-155">INPUTS</span></span>

### <span data-ttu-id="bc466-156">System.object</span><span class="sxs-lookup"><span data-stu-id="bc466-156">System.String</span></span>

### <span data-ttu-id="bc466-157">Guid.empty</span><span class="sxs-lookup"><span data-stu-id="bc466-157">System.Guid</span></span>

### <span data-ttu-id="bc466-158">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="bc466-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="bc466-159">SecureString</span><span class="sxs-lookup"><span data-stu-id="bc466-159">System.Security.SecureString</span></span>

### <span data-ttu-id="bc466-160">System.object</span><span class="sxs-lookup"><span data-stu-id="bc466-160">System.DateTime</span></span>

## <span data-ttu-id="bc466-161">輸出</span><span class="sxs-lookup"><span data-stu-id="bc466-161">OUTPUTS</span></span>

### <span data-ttu-id="bc466-162">PSADCredential （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="bc466-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="bc466-163">筆記</span><span class="sxs-lookup"><span data-stu-id="bc466-163">NOTES</span></span>

## <span data-ttu-id="bc466-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="bc466-164">RELATED LINKS</span></span>

[<span data-ttu-id="bc466-165">AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bc466-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="bc466-166">移除-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="bc466-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="bc466-167">AzADApplication</span><span class="sxs-lookup"><span data-stu-id="bc466-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

