---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: bf2a42df42a343d9745cb55f4d72463513b44dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450508"
---
# <span data-ttu-id="e81d9-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e81d9-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="e81d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e81d9-102">SYNOPSIS</span></span>
<span data-ttu-id="e81d9-103">將認證新增至現有的服務主體。</span><span class="sxs-lookup"><span data-stu-id="e81d9-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e81d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="e81d9-104">SYNTAX</span></span>

### <span data-ttu-id="e81d9-105">SpObjectIdWithPasswordParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="e81d9-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e81d9-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="e81d9-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e81d9-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="e81d9-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e81d9-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="e81d9-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e81d9-109">說明</span><span class="sxs-lookup"><span data-stu-id="e81d9-109">DESCRIPTION</span></span>
<span data-ttu-id="e81d9-110">New-AzureRmADSpCredential Cmdlet 可以用來新增認證，或為服務主體轉移認證。</span><span class="sxs-lookup"><span data-stu-id="e81d9-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="e81d9-111">服務主體是透過提供物件識別碼或服務主體名稱來識別。</span><span class="sxs-lookup"><span data-stu-id="e81d9-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="e81d9-112">示例</span><span class="sxs-lookup"><span data-stu-id="e81d9-112">EXAMPLES</span></span>

### <span data-ttu-id="e81d9-113">範例1</span><span class="sxs-lookup"><span data-stu-id="e81d9-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $SecureStringPassword
```

<span data-ttu-id="e81d9-114">新的密碼認證已新增至現有的服務主體。</span><span class="sxs-lookup"><span data-stu-id="e81d9-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="e81d9-115">在這個範例中，會將提供的密碼值新增到使用 objectId 的服務主體。</span><span class="sxs-lookup"><span data-stu-id="e81d9-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="e81d9-116">範例2</span><span class="sxs-lookup"><span data-stu-id="e81d9-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="e81d9-117">現有的服務主體會新增新的金鑰認證。</span><span class="sxs-lookup"><span data-stu-id="e81d9-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="e81d9-118">在這個範例中，提供的 base64 編碼公用 X509 憑證 ( "myapp" ) 是使用其 SPN 新增至服務主體。</span><span class="sxs-lookup"><span data-stu-id="e81d9-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="e81d9-119">範例3</span><span class="sxs-lookup"><span data-stu-id="e81d9-119">Example 3</span></span>

```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="e81d9-120">參數</span><span class="sxs-lookup"><span data-stu-id="e81d9-120">PARAMETERS</span></span>

### <span data-ttu-id="e81d9-121">-CertValue</span><span class="sxs-lookup"><span data-stu-id="e81d9-121">-CertValue</span></span>
<span data-ttu-id="e81d9-122">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="e81d9-122">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="e81d9-123">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="e81d9-123">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81d9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e81d9-124">-DefaultProfile</span></span>
<span data-ttu-id="e81d9-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e81d9-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e81d9-126">-結束日期</span><span class="sxs-lookup"><span data-stu-id="e81d9-126">-EndDate</span></span>
<span data-ttu-id="e81d9-127">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="e81d9-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="e81d9-128">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="e81d9-128">The default end date value is one year from today.</span></span> <span data-ttu-id="e81d9-129">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="e81d9-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81d9-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e81d9-130">-ObjectId</span></span>
<span data-ttu-id="e81d9-131">要新增認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="e81d9-131">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81d9-132">-Password</span><span class="sxs-lookup"><span data-stu-id="e81d9-132">-Password</span></span>
<span data-ttu-id="e81d9-133">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="e81d9-133">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81d9-134">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e81d9-134">-ServicePrincipalName</span></span>
<span data-ttu-id="e81d9-135">要新增認證之服務主體 (SPN) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e81d9-135">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81d9-136">-開始日期</span><span class="sxs-lookup"><span data-stu-id="e81d9-136">-StartDate</span></span>
<span data-ttu-id="e81d9-137">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="e81d9-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="e81d9-138">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="e81d9-138">The default start date value is today.</span></span> <span data-ttu-id="e81d9-139">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="e81d9-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e81d9-140">-確認</span><span class="sxs-lookup"><span data-stu-id="e81d9-140">-Confirm</span></span>
<span data-ttu-id="e81d9-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e81d9-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e81d9-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81d9-142">-WhatIf</span></span>
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

### <span data-ttu-id="e81d9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81d9-143">CommonParameters</span></span>
<span data-ttu-id="e81d9-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e81d9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81d9-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e81d9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81d9-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e81d9-146">INPUTS</span></span>

### <span data-ttu-id="e81d9-147">所有</span><span class="sxs-lookup"><span data-stu-id="e81d9-147">None</span></span>
<span data-ttu-id="e81d9-148">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e81d9-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e81d9-149">輸出</span><span class="sxs-lookup"><span data-stu-id="e81d9-149">OUTPUTS</span></span>

### <span data-ttu-id="e81d9-150">Microsoft.Azure.Graph.RBAC.Version1_6 PSADCredential</span><span class="sxs-lookup"><span data-stu-id="e81d9-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e81d9-151">筆記</span><span class="sxs-lookup"><span data-stu-id="e81d9-151">NOTES</span></span>

## <span data-ttu-id="e81d9-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="e81d9-152">RELATED LINKS</span></span>

[<span data-ttu-id="e81d9-153">AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e81d9-153">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="e81d9-154">移除-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e81d9-154">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="e81d9-155">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e81d9-155">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



