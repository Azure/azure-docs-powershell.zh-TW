---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: fa861a7be0716ec1da1f2f2a100e7dbbdc97af51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620853"
---
# <span data-ttu-id="7fb70-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7fb70-101">New-AzADApplication</span></span>

## <span data-ttu-id="7fb70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7fb70-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb70-103">建立新的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="7fb70-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="7fb70-104">句法</span><span class="sxs-lookup"><span data-stu-id="7fb70-104">SYNTAX</span></span>

### <span data-ttu-id="7fb70-105">ApplicationWithoutCredentialParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7fb70-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb70-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb70-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb70-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb70-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb70-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb70-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fb70-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb70-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb70-110">說明</span><span class="sxs-lookup"><span data-stu-id="7fb70-110">DESCRIPTION</span></span>
<span data-ttu-id="7fb70-111">建立新的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="7fb70-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="7fb70-112">示例</span><span class="sxs-lookup"><span data-stu-id="7fb70-112">EXAMPLES</span></span>

### <span data-ttu-id="7fb70-113">範例 1-建立新的 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="7fb70-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="7fb70-114">建立不含任何認證的新 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="7fb70-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="7fb70-115">範例 2-使用密碼建立新的 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="7fb70-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="7fb70-116">建立新的 azure active directory 應用程式，並將密碼認證與它相關聯。</span><span class="sxs-lookup"><span data-stu-id="7fb70-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="7fb70-117">參數</span><span class="sxs-lookup"><span data-stu-id="7fb70-117">PARAMETERS</span></span>

### <span data-ttu-id="7fb70-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="7fb70-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="7fb70-119">指定應用程式是單一租使用者還是多租使用者的值。</span><span class="sxs-lookup"><span data-stu-id="7fb70-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb70-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="7fb70-120">-CertValue</span></span>
<span data-ttu-id="7fb70-121">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="7fb70-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="7fb70-122">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="7fb70-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb70-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb70-123">-DefaultProfile</span></span>
<span data-ttu-id="7fb70-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7fb70-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fb70-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7fb70-125">-DisplayName</span></span>
<span data-ttu-id="7fb70-126">新應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="7fb70-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="7fb70-127">-結束日期</span><span class="sxs-lookup"><span data-stu-id="7fb70-127">-EndDate</span></span>
<span data-ttu-id="7fb70-128">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="7fb70-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="7fb70-129">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="7fb70-129">The default end date value is one year from today.</span></span> <span data-ttu-id="7fb70-130">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="7fb70-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb70-131">-首頁</span><span class="sxs-lookup"><span data-stu-id="7fb70-131">-HomePage</span></span>
<span data-ttu-id="7fb70-132">應用程式首頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="7fb70-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="7fb70-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="7fb70-133">-IdentifierUris</span></span>
<span data-ttu-id="7fb70-134">識別應用程式的 Uri。</span><span class="sxs-lookup"><span data-stu-id="7fb70-134">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb70-135">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="7fb70-135">-KeyCredentials</span></span>
<span data-ttu-id="7fb70-136">與應用程式相關聯的憑證認證清單。</span><span class="sxs-lookup"><span data-stu-id="7fb70-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb70-137">-Password</span><span class="sxs-lookup"><span data-stu-id="7fb70-137">-Password</span></span>
<span data-ttu-id="7fb70-138">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="7fb70-138">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb70-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="7fb70-139">-PasswordCredentials</span></span>
<span data-ttu-id="7fb70-140">與應用程式相關聯的密碼認證清單。</span><span class="sxs-lookup"><span data-stu-id="7fb70-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb70-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="7fb70-141">-ReplyUrls</span></span>
<span data-ttu-id="7fb70-142">應用程式回復 url。</span><span class="sxs-lookup"><span data-stu-id="7fb70-142">The application reply urls.</span></span>

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

### <span data-ttu-id="7fb70-143">-開始日期</span><span class="sxs-lookup"><span data-stu-id="7fb70-143">-StartDate</span></span>
<span data-ttu-id="7fb70-144">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="7fb70-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="7fb70-145">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="7fb70-145">The default start date value is today.</span></span> <span data-ttu-id="7fb70-146">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="7fb70-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fb70-147">-確認</span><span class="sxs-lookup"><span data-stu-id="7fb70-147">-Confirm</span></span>
<span data-ttu-id="7fb70-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7fb70-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb70-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb70-149">-WhatIf</span></span>
<span data-ttu-id="7fb70-150">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7fb70-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fb70-151">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7fb70-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb70-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb70-152">CommonParameters</span></span>
<span data-ttu-id="7fb70-153">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7fb70-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb70-154">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7fb70-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb70-155">輸入</span><span class="sxs-lookup"><span data-stu-id="7fb70-155">INPUTS</span></span>

### <span data-ttu-id="7fb70-156">System.object</span><span class="sxs-lookup"><span data-stu-id="7fb70-156">System.String</span></span>

### <span data-ttu-id="7fb70-157">System.object []</span><span class="sxs-lookup"><span data-stu-id="7fb70-157">System.String[]</span></span>

### <span data-ttu-id="7fb70-158">System.object</span><span class="sxs-lookup"><span data-stu-id="7fb70-158">System.Boolean</span></span>

### <span data-ttu-id="7fb70-159">PSADPasswordCredential [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7fb70-159">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="7fb70-160">PSADKeyCredential [] （[]）</span><span class="sxs-lookup"><span data-stu-id="7fb70-160">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="7fb70-161">SecureString</span><span class="sxs-lookup"><span data-stu-id="7fb70-161">System.Security.SecureString</span></span>

### <span data-ttu-id="7fb70-162">System.object</span><span class="sxs-lookup"><span data-stu-id="7fb70-162">System.DateTime</span></span>

## <span data-ttu-id="7fb70-163">輸出</span><span class="sxs-lookup"><span data-stu-id="7fb70-163">OUTPUTS</span></span>

### <span data-ttu-id="7fb70-164">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="7fb70-164">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="7fb70-165">筆記</span><span class="sxs-lookup"><span data-stu-id="7fb70-165">NOTES</span></span>
<span data-ttu-id="7fb70-166">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="7fb70-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7fb70-167">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fb70-167">RELATED LINKS</span></span>

[<span data-ttu-id="7fb70-168">移除-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7fb70-168">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="7fb70-169">AzADApplication</span><span class="sxs-lookup"><span data-stu-id="7fb70-169">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="7fb70-170">新-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="7fb70-170">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="7fb70-171">AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7fb70-171">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="7fb70-172">新-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7fb70-172">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="7fb70-173">移除-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="7fb70-173">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

