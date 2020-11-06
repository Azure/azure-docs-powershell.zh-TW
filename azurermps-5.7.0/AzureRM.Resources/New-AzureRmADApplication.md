---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: 171f09e2d9a9e6e646731817526451b311f94482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452071"
---
# <span data-ttu-id="690fa-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="690fa-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="690fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="690fa-102">SYNOPSIS</span></span>
<span data-ttu-id="690fa-103">建立新的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="690fa-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="690fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="690fa-104">SYNTAX</span></span>

### <span data-ttu-id="690fa-105">ApplicationWithoutCredentialParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="690fa-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="690fa-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="690fa-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="690fa-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="690fa-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="690fa-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="690fa-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="690fa-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="690fa-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="690fa-110">說明</span><span class="sxs-lookup"><span data-stu-id="690fa-110">DESCRIPTION</span></span>
<span data-ttu-id="690fa-111">建立新的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="690fa-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="690fa-112">示例</span><span class="sxs-lookup"><span data-stu-id="690fa-112">EXAMPLES</span></span>

### <span data-ttu-id="690fa-113">建立新的 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="690fa-113">Create new AAD application.</span></span>
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="690fa-114">建立不含任何認證的新 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="690fa-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="690fa-115">使用密碼建立新的 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="690fa-115">Create new AAD application with password.</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="690fa-116">建立新的 azure active directory 應用程式，並將密碼認證與它相關聯。</span><span class="sxs-lookup"><span data-stu-id="690fa-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="690fa-117">參數</span><span class="sxs-lookup"><span data-stu-id="690fa-117">PARAMETERS</span></span>

### <span data-ttu-id="690fa-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="690fa-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="690fa-119">指定應用程式是單一租使用者還是多租使用者的值。</span><span class="sxs-lookup"><span data-stu-id="690fa-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="690fa-120">-CertValue</span></span>
<span data-ttu-id="690fa-121">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="690fa-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="690fa-122">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="690fa-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="690fa-123">-DefaultProfile</span></span>
<span data-ttu-id="690fa-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="690fa-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="690fa-125">-DisplayName</span></span>
<span data-ttu-id="690fa-126">新應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="690fa-126">Display name of the new application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-127">-結束日期</span><span class="sxs-lookup"><span data-stu-id="690fa-127">-EndDate</span></span>
<span data-ttu-id="690fa-128">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="690fa-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="690fa-129">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="690fa-129">The default end date value is one year from today.</span></span> <span data-ttu-id="690fa-130">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="690fa-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-131">-首頁</span><span class="sxs-lookup"><span data-stu-id="690fa-131">-HomePage</span></span>
<span data-ttu-id="690fa-132">應用程式首頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="690fa-132">The URL to the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="690fa-133">-IdentifierUris</span></span>
<span data-ttu-id="690fa-134">識別應用程式的 Uri。</span><span class="sxs-lookup"><span data-stu-id="690fa-134">The URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-135">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="690fa-135">-KeyCredentials</span></span>
<span data-ttu-id="690fa-136">與應用程式相關聯的憑證認證清單。</span><span class="sxs-lookup"><span data-stu-id="690fa-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-137">-Password</span><span class="sxs-lookup"><span data-stu-id="690fa-137">-Password</span></span>
<span data-ttu-id="690fa-138">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="690fa-138">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="690fa-139">-PasswordCredentials</span></span>
<span data-ttu-id="690fa-140">與應用程式相關聯的密碼認證清單。</span><span class="sxs-lookup"><span data-stu-id="690fa-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="690fa-141">-ReplyUrls</span></span>
<span data-ttu-id="690fa-142">應用程式回復 url。</span><span class="sxs-lookup"><span data-stu-id="690fa-142">The application reply urls.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-143">-開始日期</span><span class="sxs-lookup"><span data-stu-id="690fa-143">-StartDate</span></span>
<span data-ttu-id="690fa-144">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="690fa-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="690fa-145">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="690fa-145">The default start date value is today.</span></span> <span data-ttu-id="690fa-146">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="690fa-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-147">-確認</span><span class="sxs-lookup"><span data-stu-id="690fa-147">-Confirm</span></span>
<span data-ttu-id="690fa-148">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="690fa-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="690fa-149">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="690fa-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="690fa-150">CommonParameters</span></span>
<span data-ttu-id="690fa-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="690fa-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="690fa-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="690fa-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="690fa-153">輸入</span><span class="sxs-lookup"><span data-stu-id="690fa-153">INPUTS</span></span>

### <span data-ttu-id="690fa-154">所有</span><span class="sxs-lookup"><span data-stu-id="690fa-154">None</span></span>
<span data-ttu-id="690fa-155">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="690fa-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="690fa-156">輸出</span><span class="sxs-lookup"><span data-stu-id="690fa-156">OUTPUTS</span></span>

### <span data-ttu-id="690fa-157">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="690fa-157">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="690fa-158">筆記</span><span class="sxs-lookup"><span data-stu-id="690fa-158">NOTES</span></span>
<span data-ttu-id="690fa-159">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="690fa-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="690fa-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="690fa-160">RELATED LINKS</span></span>

[<span data-ttu-id="690fa-161">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="690fa-161">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="690fa-162">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="690fa-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="690fa-163">新-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="690fa-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="690fa-164">AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="690fa-164">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="690fa-165">新-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="690fa-165">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="690fa-166">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="690fa-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

