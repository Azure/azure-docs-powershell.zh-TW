---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: ca338fd648010b9158a6bc308bb4dcb2f1c48317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452067"
---
# <span data-ttu-id="5d499-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d499-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="5d499-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d499-102">SYNOPSIS</span></span>
<span data-ttu-id="5d499-103">建立新的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="5d499-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d499-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d499-104">SYNTAX</span></span>

### <span data-ttu-id="5d499-105">ApplicationWithoutCredentialParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="5d499-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d499-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d499-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d499-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d499-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d499-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d499-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d499-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d499-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d499-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d499-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d499-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d499-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d499-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d499-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d499-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d499-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d499-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d499-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d499-115">說明</span><span class="sxs-lookup"><span data-stu-id="5d499-115">DESCRIPTION</span></span>
<span data-ttu-id="5d499-116">建立新的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="5d499-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="5d499-117">注意：如果沒有提供 ApplicationId，此 Cmdlet 也會以隱含方式建立應用程式，並將其屬性 () 。</span><span class="sxs-lookup"><span data-stu-id="5d499-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="5d499-118">若要更新應用程式的特定參數，請使用 Set-AzureRmADApplication Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d499-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="5d499-119">示例</span><span class="sxs-lookup"><span data-stu-id="5d499-119">EXAMPLES</span></span>

### <span data-ttu-id="5d499-120">範例1</span><span class="sxs-lookup"><span data-stu-id="5d499-120">Example 1</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="5d499-121">建立新的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="5d499-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="5d499-122">DisplayName 類型 ObjectId</span><span class="sxs-lookup"><span data-stu-id="5d499-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="5d499-123">DemoApp ServicePrincipal f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="5d499-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="5d499-124">範例2</span><span class="sxs-lookup"><span data-stu-id="5d499-124">Example 2</span></span>
```
$SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp -Password $SecureStringPassword
```

<span data-ttu-id="5d499-125">建立新的服務主體。</span><span class="sxs-lookup"><span data-stu-id="5d499-125">Creates a new service principal.</span></span>
<span data-ttu-id="5d499-126">這個 Cmdlet 也會隱式建立一個應用程式，因為沒有提供。</span><span class="sxs-lookup"><span data-stu-id="5d499-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="5d499-127">DisplayName 類型 ObjectId</span><span class="sxs-lookup"><span data-stu-id="5d499-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="5d499-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="5d499-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="5d499-129">參數</span><span class="sxs-lookup"><span data-stu-id="5d499-129">PARAMETERS</span></span>

### <span data-ttu-id="5d499-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5d499-130">-ApplicationId</span></span>
<span data-ttu-id="5d499-131">租使用者中服務主體的唯一應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="5d499-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="5d499-132">建立之後，就無法變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5d499-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="5d499-133">如果沒有指定應用程式識別碼，就會產生一個。</span><span class="sxs-lookup"><span data-stu-id="5d499-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d499-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="5d499-134">-CertValue</span></span>
<span data-ttu-id="5d499-135">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="5d499-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="5d499-136">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="5d499-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d499-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d499-137">-DefaultProfile</span></span>
<span data-ttu-id="5d499-138">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5d499-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d499-139">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5d499-139">-DisplayName</span></span>
<span data-ttu-id="5d499-140">服務主體的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="5d499-140">The friendly name of the service principal.</span></span>

```yaml
Type: String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d499-141">-結束日期</span><span class="sxs-lookup"><span data-stu-id="5d499-141">-EndDate</span></span>
<span data-ttu-id="5d499-142">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="5d499-142">The effective end date of the credential usage.</span></span>
<span data-ttu-id="5d499-143">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="5d499-143">The default end date value is one year from today.</span></span> <span data-ttu-id="5d499-144">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="5d499-144">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d499-145">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="5d499-145">-KeyCredentials</span></span>
<span data-ttu-id="5d499-146">與服務主體相關聯的憑證認證清單。</span><span class="sxs-lookup"><span data-stu-id="5d499-146">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d499-147">-Password</span><span class="sxs-lookup"><span data-stu-id="5d499-147">-Password</span></span>
<span data-ttu-id="5d499-148">要與服務主體相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="5d499-148">The password to be associated with the service principal.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d499-149">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="5d499-149">-PasswordCredentials</span></span>
<span data-ttu-id="5d499-150">與服務主體相關聯的密碼認證清單。</span><span class="sxs-lookup"><span data-stu-id="5d499-150">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d499-151">-開始日期</span><span class="sxs-lookup"><span data-stu-id="5d499-151">-StartDate</span></span>
<span data-ttu-id="5d499-152">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="5d499-152">The effective start date of the credential usage.</span></span>
<span data-ttu-id="5d499-153">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="5d499-153">The default start date value is today.</span></span> <span data-ttu-id="5d499-154">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="5d499-154">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d499-155">-確認</span><span class="sxs-lookup"><span data-stu-id="5d499-155">-Confirm</span></span>
<span data-ttu-id="5d499-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5d499-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d499-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d499-157">-WhatIf</span></span>
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

### <span data-ttu-id="5d499-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d499-158">CommonParameters</span></span>
<span data-ttu-id="5d499-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d499-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d499-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5d499-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d499-161">輸入</span><span class="sxs-lookup"><span data-stu-id="5d499-161">INPUTS</span></span>

### <span data-ttu-id="5d499-162">所有</span><span class="sxs-lookup"><span data-stu-id="5d499-162">None</span></span>
<span data-ttu-id="5d499-163">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5d499-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d499-164">輸出</span><span class="sxs-lookup"><span data-stu-id="5d499-164">OUTPUTS</span></span>

### <span data-ttu-id="5d499-165">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d499-165">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="5d499-166">筆記</span><span class="sxs-lookup"><span data-stu-id="5d499-166">NOTES</span></span>
<span data-ttu-id="5d499-167">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="5d499-167">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5d499-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d499-168">RELATED LINKS</span></span>

[<span data-ttu-id="5d499-169">移除-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d499-169">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="5d499-170">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d499-170">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="5d499-171">新-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5d499-171">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="5d499-172">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5d499-172">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="5d499-173">AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5d499-173">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="5d499-174">新-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5d499-174">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="5d499-175">移除-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5d499-175">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

