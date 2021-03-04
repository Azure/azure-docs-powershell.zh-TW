---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: c2b3ebfafc1e5e11cbed69fce0cb935cf48131be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910366"
---
# <span data-ttu-id="61a10-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="61a10-101">New-AzADApplication</span></span>

## <span data-ttu-id="61a10-102">簡介</span><span class="sxs-lookup"><span data-stu-id="61a10-102">SYNOPSIS</span></span>
<span data-ttu-id="61a10-103">建立新 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="61a10-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="61a10-104">語法</span><span class="sxs-lookup"><span data-stu-id="61a10-104">SYNTAX</span></span>

### <span data-ttu-id="61a10-105">ApplicationWithoutCredentialParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="61a10-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a10-106">ApplicationWithPasswordP有ParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a10-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a10-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a10-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a10-108">ApplicationWithKeyP有ParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a10-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61a10-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="61a10-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61a10-110">描述</span><span class="sxs-lookup"><span data-stu-id="61a10-110">DESCRIPTION</span></span>
<span data-ttu-id="61a10-111">建立新 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="61a10-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="61a10-112">以下是建立應用程式所需的許可權：</span><span class="sxs-lookup"><span data-stu-id="61a10-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="61a10-113">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="61a10-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="61a10-114">Application.ReadWrite.OwnedBy</span><span class="sxs-lookup"><span data-stu-id="61a10-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="61a10-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="61a10-115">Microsoft Graph</span></span>
  - <span data-ttu-id="61a10-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="61a10-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="61a10-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61a10-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="61a10-118">例子</span><span class="sxs-lookup"><span data-stu-id="61a10-118">EXAMPLES</span></span>

### <span data-ttu-id="61a10-119">範例 1：建立新 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="61a10-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="61a10-120">建立不含任何認證的新 Azure Active Directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="61a10-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="61a10-121">範例 2：使用密碼建立新 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="61a10-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="61a10-122">建立新的 Azure Active Directory 應用程式，並關聯密碼認證。</span><span class="sxs-lookup"><span data-stu-id="61a10-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="61a10-123">參數</span><span class="sxs-lookup"><span data-stu-id="61a10-123">PARAMETERS</span></span>

### <span data-ttu-id="61a10-124">-AvailableToTentenants</span><span class="sxs-lookup"><span data-stu-id="61a10-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="61a10-125">指定應用程式是單一租使用者或多租使用者的值。</span><span class="sxs-lookup"><span data-stu-id="61a10-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="61a10-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="61a10-126">-CertValue</span></span>
<span data-ttu-id="61a10-127">「非對稱」認證類型的值。</span><span class="sxs-lookup"><span data-stu-id="61a10-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="61a10-128">它代表基礎 64 編碼憑證。</span><span class="sxs-lookup"><span data-stu-id="61a10-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="61a10-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61a10-129">-DefaultProfile</span></span>
<span data-ttu-id="61a10-130">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="61a10-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61a10-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="61a10-131">-DisplayName</span></span>
<span data-ttu-id="61a10-132">新應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="61a10-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="61a10-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="61a10-133">-EndDate</span></span>
<span data-ttu-id="61a10-134">認證使用量的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="61a10-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="61a10-135">預設結束日期為自今天起一年。</span><span class="sxs-lookup"><span data-stu-id="61a10-135">The default end date value is one year from today.</span></span> <span data-ttu-id="61a10-136">對於「非對稱」類型認證，這必須設定為 X509 憑證有效日期當天或之前。</span><span class="sxs-lookup"><span data-stu-id="61a10-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="61a10-137">-HomePage</span><span class="sxs-lookup"><span data-stu-id="61a10-137">-HomePage</span></span>
<span data-ttu-id="61a10-138">應用程式首頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="61a10-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="61a10-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="61a10-139">-IdentifierUris</span></span>
<span data-ttu-id="61a10-140">識別應用程式的 URI。</span><span class="sxs-lookup"><span data-stu-id="61a10-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="61a10-141">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="61a10-141">-KeyCredentials</span></span>
<span data-ttu-id="61a10-142">與應用程式相關聯的憑證認證清單。</span><span class="sxs-lookup"><span data-stu-id="61a10-142">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="61a10-143">-密碼</span><span class="sxs-lookup"><span data-stu-id="61a10-143">-Password</span></span>
<span data-ttu-id="61a10-144">與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="61a10-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="61a10-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="61a10-145">-PasswordCredentials</span></span>
<span data-ttu-id="61a10-146">與應用程式相關聯的密碼認證清單。</span><span class="sxs-lookup"><span data-stu-id="61a10-146">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="61a10-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="61a10-147">-ReplyUrls</span></span>
<span data-ttu-id="61a10-148">應用程式回復 URL。</span><span class="sxs-lookup"><span data-stu-id="61a10-148">The application reply urls.</span></span>

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

### <span data-ttu-id="61a10-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="61a10-149">-StartDate</span></span>
<span data-ttu-id="61a10-150">認證使用量的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="61a10-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="61a10-151">預設的開始日期值是今天。</span><span class="sxs-lookup"><span data-stu-id="61a10-151">The default start date value is today.</span></span> <span data-ttu-id="61a10-152">對於「非對稱」類型認證，這必須設定為 X509 憑證的有效日期當天或之後。</span><span class="sxs-lookup"><span data-stu-id="61a10-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="61a10-153">-確認</span><span class="sxs-lookup"><span data-stu-id="61a10-153">-Confirm</span></span>
<span data-ttu-id="61a10-154">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="61a10-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61a10-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61a10-155">-WhatIf</span></span>
<span data-ttu-id="61a10-156">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61a10-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61a10-157">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61a10-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61a10-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61a10-158">CommonParameters</span></span>
<span data-ttu-id="61a10-159">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="61a10-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61a10-160">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61a10-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61a10-161">輸入</span><span class="sxs-lookup"><span data-stu-id="61a10-161">INPUTS</span></span>

### <span data-ttu-id="61a10-162">System.String</span><span class="sxs-lookup"><span data-stu-id="61a10-162">System.String</span></span>

### <span data-ttu-id="61a10-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="61a10-163">System.String[]</span></span>

### <span data-ttu-id="61a10-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61a10-164">System.Boolean</span></span>

### <span data-ttu-id="61a10-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="61a10-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="61a10-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="61a10-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="61a10-167">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="61a10-167">System.Security.SecureString</span></span>

### <span data-ttu-id="61a10-168">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="61a10-168">System.DateTime</span></span>

## <span data-ttu-id="61a10-169">輸出</span><span class="sxs-lookup"><span data-stu-id="61a10-169">OUTPUTS</span></span>

### <span data-ttu-id="61a10-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="61a10-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="61a10-171">筆記</span><span class="sxs-lookup"><span data-stu-id="61a10-171">NOTES</span></span>
<span data-ttu-id="61a10-172">關鍵字：azure、azurerm、arm、資源、管理、管理員、資源、群組、範本、部署</span><span class="sxs-lookup"><span data-stu-id="61a10-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="61a10-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="61a10-173">RELATED LINKS</span></span>

[<span data-ttu-id="61a10-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="61a10-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="61a10-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="61a10-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="61a10-176">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="61a10-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="61a10-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="61a10-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="61a10-178">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="61a10-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="61a10-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="61a10-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

