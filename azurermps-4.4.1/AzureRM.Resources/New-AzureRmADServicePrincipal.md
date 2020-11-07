---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: 4b327193a8dcbfecae8f13fa234da703d1a93cfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626230"
---
# <span data-ttu-id="226e2-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="226e2-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="226e2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="226e2-102">SYNOPSIS</span></span>
<span data-ttu-id="226e2-103">建立新的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="226e2-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="226e2-104">句法</span><span class="sxs-lookup"><span data-stu-id="226e2-104">SYNTAX</span></span>

### <span data-ttu-id="226e2-105">ApplicationWithoutCredentialParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="226e2-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="226e2-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="226e2-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="226e2-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="226e2-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="226e2-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="226e2-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="226e2-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="226e2-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="226e2-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="226e2-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="226e2-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="226e2-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="226e2-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="226e2-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="226e2-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="226e2-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="226e2-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="226e2-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="226e2-115">說明</span><span class="sxs-lookup"><span data-stu-id="226e2-115">DESCRIPTION</span></span>
<span data-ttu-id="226e2-116">建立新的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="226e2-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="226e2-117">注意：如果沒有提供 ApplicationId，此 Cmdlet 也會以隱含方式建立應用程式，並將其屬性 () 。</span><span class="sxs-lookup"><span data-stu-id="226e2-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="226e2-118">若要更新應用程式的特定參數，請使用 Set-AzureRmADApplication Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="226e2-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="226e2-119">示例</span><span class="sxs-lookup"><span data-stu-id="226e2-119">EXAMPLES</span></span>

### <span data-ttu-id="226e2-120">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="226e2-120">--------------------------  Example 1  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="226e2-121">建立新的 azure active directory 服務主體。</span><span class="sxs-lookup"><span data-stu-id="226e2-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="226e2-122">DisplayName 類型 ObjectId</span><span class="sxs-lookup"><span data-stu-id="226e2-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="226e2-123">DemoApp ServicePrincipal f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="226e2-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="226e2-124">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="226e2-124">--------------------------  Example 2  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp
```

<span data-ttu-id="226e2-125">建立新的服務主體。</span><span class="sxs-lookup"><span data-stu-id="226e2-125">Creates a new service principal.</span></span>
<span data-ttu-id="226e2-126">這個 Cmdlet 也會隱式建立一個應用程式，因為沒有提供。</span><span class="sxs-lookup"><span data-stu-id="226e2-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="226e2-127">DisplayName 類型 ObjectId</span><span class="sxs-lookup"><span data-stu-id="226e2-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="226e2-128">SPForNoExistingApp ServicePrincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="226e2-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="226e2-129">參數</span><span class="sxs-lookup"><span data-stu-id="226e2-129">PARAMETERS</span></span>

### <span data-ttu-id="226e2-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="226e2-130">-ApplicationId</span></span>
<span data-ttu-id="226e2-131">租使用者中服務主體的唯一應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="226e2-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="226e2-132">建立之後，就無法變更這個屬性。</span><span class="sxs-lookup"><span data-stu-id="226e2-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="226e2-133">如果沒有指定應用程式識別碼，就會產生一個。</span><span class="sxs-lookup"><span data-stu-id="226e2-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226e2-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="226e2-134">-CertValue</span></span>
<span data-ttu-id="226e2-135">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="226e2-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="226e2-136">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="226e2-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226e2-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="226e2-137">-DisplayName</span></span>
<span data-ttu-id="226e2-138">服務主體的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="226e2-138">The friendly name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226e2-139">-結束日期</span><span class="sxs-lookup"><span data-stu-id="226e2-139">-EndDate</span></span>
<span data-ttu-id="226e2-140">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="226e2-140">The effective end date of the credential usage.</span></span>
<span data-ttu-id="226e2-141">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="226e2-141">The default end date value is one year from today.</span></span> <span data-ttu-id="226e2-142">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="226e2-142">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226e2-143">-KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="226e2-143">-KeyCredentials</span></span>
<span data-ttu-id="226e2-144">與服務主體相關聯的憑證認證清單。</span><span class="sxs-lookup"><span data-stu-id="226e2-144">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226e2-145">-Password</span><span class="sxs-lookup"><span data-stu-id="226e2-145">-Password</span></span>
<span data-ttu-id="226e2-146">要與服務主體相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="226e2-146">The password to be associated with the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226e2-147">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="226e2-147">-PasswordCredentials</span></span>
<span data-ttu-id="226e2-148">與服務主體相關聯的密碼認證清單。</span><span class="sxs-lookup"><span data-stu-id="226e2-148">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226e2-149">-開始日期</span><span class="sxs-lookup"><span data-stu-id="226e2-149">-StartDate</span></span>
<span data-ttu-id="226e2-150">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="226e2-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="226e2-151">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="226e2-151">The default start date value is today.</span></span> <span data-ttu-id="226e2-152">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="226e2-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="226e2-153">-確認</span><span class="sxs-lookup"><span data-stu-id="226e2-153">-Confirm</span></span>
<span data-ttu-id="226e2-154">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="226e2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="226e2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="226e2-155">-WhatIf</span></span>
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

### <span data-ttu-id="226e2-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="226e2-156">-DefaultProfile</span></span>
<span data-ttu-id="226e2-157">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="226e2-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="226e2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226e2-158">CommonParameters</span></span>
<span data-ttu-id="226e2-159">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="226e2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226e2-160">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="226e2-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226e2-161">輸入</span><span class="sxs-lookup"><span data-stu-id="226e2-161">INPUTS</span></span>

## <span data-ttu-id="226e2-162">輸出</span><span class="sxs-lookup"><span data-stu-id="226e2-162">OUTPUTS</span></span>

### <span data-ttu-id="226e2-163">Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="226e2-163">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="226e2-164">筆記</span><span class="sxs-lookup"><span data-stu-id="226e2-164">NOTES</span></span>
<span data-ttu-id="226e2-165">關鍵字： azure，azurerm，arm，資源，管理，管理員，資源，群組，範本，部署</span><span class="sxs-lookup"><span data-stu-id="226e2-165">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="226e2-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="226e2-166">RELATED LINKS</span></span>

[<span data-ttu-id="226e2-167">移除-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="226e2-167">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="226e2-168">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="226e2-168">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="226e2-169">新-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="226e2-169">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="226e2-170">移除-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="226e2-170">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="226e2-171">AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="226e2-171">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="226e2-172">新-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="226e2-172">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="226e2-173">移除-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="226e2-173">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

