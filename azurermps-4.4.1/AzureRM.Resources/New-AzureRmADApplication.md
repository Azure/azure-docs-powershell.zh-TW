---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: c43bba247268d7ffcdbc2c33d7198415738c5694
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456415"
---
# <span data-ttu-id="f820e-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f820e-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="f820e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f820e-102">SYNOPSIS</span></span>
<span data-ttu-id="f820e-103">建立新的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f820e-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f820e-104">句法</span><span class="sxs-lookup"><span data-stu-id="f820e-104">SYNTAX</span></span>

### <span data-ttu-id="f820e-105">ApplicationWithoutCredentialParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f820e-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f820e-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="f820e-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f820e-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="f820e-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f820e-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="f820e-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f820e-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="f820e-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f820e-110">說明</span><span class="sxs-lookup"><span data-stu-id="f820e-110">DESCRIPTION</span></span>
<span data-ttu-id="f820e-111">建立新的 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f820e-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="f820e-112">示例</span><span class="sxs-lookup"><span data-stu-id="f820e-112">EXAMPLES</span></span>

### <span data-ttu-id="f820e-113">--------------------------建立新的 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f820e-113">--------------------------  Create new AAD application.</span></span>  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="f820e-114">建立不含任何認證的新 azure active directory 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f820e-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="f820e-115">--------------------------使用密碼建立新的 AAD 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f820e-115">--------------------------  Create new AAD application with password.</span></span>  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password "password"
```

<span data-ttu-id="f820e-116">建立新的 azure active directory 應用程式，並將密碼認證與它相關聯。</span><span class="sxs-lookup"><span data-stu-id="f820e-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="f820e-117">參數</span><span class="sxs-lookup"><span data-stu-id="f820e-117">PARAMETERS</span></span>

### <span data-ttu-id="f820e-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="f820e-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="f820e-119">指定應用程式是單一租使用者還是多租使用者的值。</span><span class="sxs-lookup"><span data-stu-id="f820e-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="f820e-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="f820e-120">-CertValue</span></span>
<span data-ttu-id="f820e-121">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="f820e-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="f820e-122">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="f820e-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="f820e-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f820e-123">-DisplayName</span></span>
<span data-ttu-id="f820e-124">新應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f820e-124">Display name of the new application.</span></span>

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

### <span data-ttu-id="f820e-125">-結束日期</span><span class="sxs-lookup"><span data-stu-id="f820e-125">-EndDate</span></span>
<span data-ttu-id="f820e-126">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="f820e-126">The effective end date of the credential usage.</span></span>
<span data-ttu-id="f820e-127">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="f820e-127">The default end date value is one year from today.</span></span> <span data-ttu-id="f820e-128">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="f820e-128">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="f820e-129">-首頁</span><span class="sxs-lookup"><span data-stu-id="f820e-129">-HomePage</span></span>
<span data-ttu-id="f820e-130">應用程式首頁的 URL。</span><span class="sxs-lookup"><span data-stu-id="f820e-130">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="f820e-131">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="f820e-131">-IdentifierUris</span></span>
<span data-ttu-id="f820e-132">識別應用程式的 Uri。</span><span class="sxs-lookup"><span data-stu-id="f820e-132">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="f820e-133">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="f820e-133">-KeyCredentials</span></span>
<span data-ttu-id="f820e-134">與應用程式相關聯的憑證認證清單。</span><span class="sxs-lookup"><span data-stu-id="f820e-134">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f820e-135">-Password</span><span class="sxs-lookup"><span data-stu-id="f820e-135">-Password</span></span>
<span data-ttu-id="f820e-136">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="f820e-136">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f820e-137">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="f820e-137">-PasswordCredentials</span></span>
<span data-ttu-id="f820e-138">與應用程式相關聯的密碼認證清單。</span><span class="sxs-lookup"><span data-stu-id="f820e-138">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f820e-139">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="f820e-139">-ReplyUrls</span></span>
<span data-ttu-id="f820e-140">應用程式回復 url。</span><span class="sxs-lookup"><span data-stu-id="f820e-140">The application reply urls.</span></span>

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

### <span data-ttu-id="f820e-141">-開始日期</span><span class="sxs-lookup"><span data-stu-id="f820e-141">-StartDate</span></span>
<span data-ttu-id="f820e-142">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="f820e-142">The effective start date of the credential usage.</span></span>
<span data-ttu-id="f820e-143">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="f820e-143">The default start date value is today.</span></span> <span data-ttu-id="f820e-144">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="f820e-144">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="f820e-145">-確認</span><span class="sxs-lookup"><span data-stu-id="f820e-145">-Confirm</span></span>
<span data-ttu-id="f820e-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f820e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f820e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f820e-147">-WhatIf</span></span>
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

### <span data-ttu-id="f820e-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f820e-148">-DefaultProfile</span></span>
<span data-ttu-id="f820e-149">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f820e-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f820e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f820e-150">CommonParameters</span></span>
<span data-ttu-id="f820e-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f820e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f820e-152">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f820e-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f820e-153">輸入</span><span class="sxs-lookup"><span data-stu-id="f820e-153">INPUTS</span></span>

## <span data-ttu-id="f820e-154">輸出</span><span class="sxs-lookup"><span data-stu-id="f820e-154">OUTPUTS</span></span>

### <span data-ttu-id="f820e-155">Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication</span><span class="sxs-lookup"><span data-stu-id="f820e-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="f820e-156">筆記</span><span class="sxs-lookup"><span data-stu-id="f820e-156">NOTES</span></span>
<span data-ttu-id="f820e-157">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="f820e-157">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f820e-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="f820e-158">RELATED LINKS</span></span>

[<span data-ttu-id="f820e-159">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f820e-159">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="f820e-160">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f820e-160">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="f820e-161">新-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f820e-161">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="f820e-162">AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f820e-162">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="f820e-163">新-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f820e-163">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="f820e-164">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f820e-164">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

