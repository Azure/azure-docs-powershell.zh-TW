---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 7ab7c679bc623a9eaa0f99bcdba1ab8281bd7d8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126917"
---
# <span data-ttu-id="05683-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="05683-101">New-AzADApplication</span></span>

## <span data-ttu-id="05683-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05683-102">SYNOPSIS</span></span>
<span data-ttu-id="05683-103">建立新的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="05683-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="05683-104">句法</span><span class="sxs-lookup"><span data-stu-id="05683-104">SYNTAX</span></span>

### <span data-ttu-id="05683-105">ApplicationWithoutCredentialParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="05683-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05683-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="05683-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05683-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="05683-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05683-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="05683-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05683-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="05683-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05683-110">說明</span><span class="sxs-lookup"><span data-stu-id="05683-110">DESCRIPTION</span></span>
<span data-ttu-id="05683-111">建立新的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="05683-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="05683-112">下列是建立應用程式所需的許可權：</span><span class="sxs-lookup"><span data-stu-id="05683-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="05683-113">Azure Active Directory 圖形</span><span class="sxs-lookup"><span data-stu-id="05683-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="05683-114">OwnedBy</span><span class="sxs-lookup"><span data-stu-id="05683-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="05683-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="05683-115">Microsoft Graph</span></span>
  - <span data-ttu-id="05683-116">AccessAsUser. All</span><span class="sxs-lookup"><span data-stu-id="05683-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="05683-117">ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="05683-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="05683-118">示例</span><span class="sxs-lookup"><span data-stu-id="05683-118">EXAMPLES</span></span>

### <span data-ttu-id="05683-119">範例1：建立新的 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="05683-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="05683-120">建立不含任何認證的新 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="05683-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="05683-121">範例2：使用密碼建立新的 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="05683-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="05683-122">建立新的 azure active directory 應用程式，並將密碼認證與它相關聯。</span><span class="sxs-lookup"><span data-stu-id="05683-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="05683-123">參數</span><span class="sxs-lookup"><span data-stu-id="05683-123">PARAMETERS</span></span>

### <span data-ttu-id="05683-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="05683-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="05683-125">指定應用程式是單一租使用者還是多租使用者的值。</span><span class="sxs-lookup"><span data-stu-id="05683-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="05683-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="05683-126">-CertValue</span></span>
<span data-ttu-id="05683-127">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="05683-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="05683-128">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="05683-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="05683-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05683-129">-DefaultProfile</span></span>
<span data-ttu-id="05683-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="05683-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05683-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="05683-131">-DisplayName</span></span>
<span data-ttu-id="05683-132">新應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="05683-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="05683-133">-結束日期</span><span class="sxs-lookup"><span data-stu-id="05683-133">-EndDate</span></span>
<span data-ttu-id="05683-134">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="05683-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="05683-135">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="05683-135">The default end date value is one year from today.</span></span> <span data-ttu-id="05683-136">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="05683-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="05683-137">-首頁</span><span class="sxs-lookup"><span data-stu-id="05683-137">-HomePage</span></span>
<span data-ttu-id="05683-138">應用程式首頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="05683-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="05683-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="05683-139">-IdentifierUris</span></span>
<span data-ttu-id="05683-140">識別應用程式的 Uri。</span><span class="sxs-lookup"><span data-stu-id="05683-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="05683-141">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="05683-141">-KeyCredentials</span></span>
<span data-ttu-id="05683-142">與應用程式相關聯的憑證認證清單。</span><span class="sxs-lookup"><span data-stu-id="05683-142">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="05683-143">-Password</span><span class="sxs-lookup"><span data-stu-id="05683-143">-Password</span></span>
<span data-ttu-id="05683-144">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="05683-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="05683-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="05683-145">-PasswordCredentials</span></span>
<span data-ttu-id="05683-146">與應用程式相關聯的密碼認證清單。</span><span class="sxs-lookup"><span data-stu-id="05683-146">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="05683-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="05683-147">-ReplyUrls</span></span>
<span data-ttu-id="05683-148">應用程式回復 url。</span><span class="sxs-lookup"><span data-stu-id="05683-148">The application reply urls.</span></span>

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

### <span data-ttu-id="05683-149">-開始日期</span><span class="sxs-lookup"><span data-stu-id="05683-149">-StartDate</span></span>
<span data-ttu-id="05683-150">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="05683-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="05683-151">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="05683-151">The default start date value is today.</span></span> <span data-ttu-id="05683-152">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="05683-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="05683-153">-確認</span><span class="sxs-lookup"><span data-stu-id="05683-153">-Confirm</span></span>
<span data-ttu-id="05683-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="05683-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05683-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05683-155">-WhatIf</span></span>
<span data-ttu-id="05683-156">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="05683-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05683-157">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05683-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05683-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05683-158">CommonParameters</span></span>
<span data-ttu-id="05683-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05683-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05683-160">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="05683-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05683-161">輸入</span><span class="sxs-lookup"><span data-stu-id="05683-161">INPUTS</span></span>

### <span data-ttu-id="05683-162">System.object</span><span class="sxs-lookup"><span data-stu-id="05683-162">System.String</span></span>

### <span data-ttu-id="05683-163">System.object []</span><span class="sxs-lookup"><span data-stu-id="05683-163">System.String[]</span></span>

### <span data-ttu-id="05683-164">System.object</span><span class="sxs-lookup"><span data-stu-id="05683-164">System.Boolean</span></span>

### <span data-ttu-id="05683-165">PSADPasswordCredential [] （[]）</span><span class="sxs-lookup"><span data-stu-id="05683-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="05683-166">PSADKeyCredential [] （[]）</span><span class="sxs-lookup"><span data-stu-id="05683-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="05683-167">SecureString</span><span class="sxs-lookup"><span data-stu-id="05683-167">System.Security.SecureString</span></span>

### <span data-ttu-id="05683-168">System.object</span><span class="sxs-lookup"><span data-stu-id="05683-168">System.DateTime</span></span>

## <span data-ttu-id="05683-169">輸出</span><span class="sxs-lookup"><span data-stu-id="05683-169">OUTPUTS</span></span>

### <span data-ttu-id="05683-170">PSADApplication （即 Azure。</span><span class="sxs-lookup"><span data-stu-id="05683-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="05683-171">筆記</span><span class="sxs-lookup"><span data-stu-id="05683-171">NOTES</span></span>
<span data-ttu-id="05683-172">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="05683-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="05683-173">相關連結</span><span class="sxs-lookup"><span data-stu-id="05683-173">RELATED LINKS</span></span>

[<span data-ttu-id="05683-174">移除-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="05683-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="05683-175">AzADApplication</span><span class="sxs-lookup"><span data-stu-id="05683-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="05683-176">新-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="05683-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="05683-177">AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="05683-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="05683-178">新-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="05683-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="05683-179">移除-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="05683-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
