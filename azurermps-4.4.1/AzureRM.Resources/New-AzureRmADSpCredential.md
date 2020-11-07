---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: 814da56d9b925e19deac81dad886604d562e05e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626228"
---
# <span data-ttu-id="21df4-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="21df4-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="21df4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21df4-102">SYNOPSIS</span></span>
<span data-ttu-id="21df4-103">將認證新增至現有的服務主體。</span><span class="sxs-lookup"><span data-stu-id="21df4-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21df4-104">句法</span><span class="sxs-lookup"><span data-stu-id="21df4-104">SYNTAX</span></span>

### <span data-ttu-id="21df4-105">SpObjectIdWithPasswordParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="21df4-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21df4-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="21df4-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21df4-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="21df4-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21df4-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="21df4-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21df4-109">說明</span><span class="sxs-lookup"><span data-stu-id="21df4-109">DESCRIPTION</span></span>
<span data-ttu-id="21df4-110">New-AzureRmADSpCredential Cmdlet 可以用來新增認證，或為服務主體轉移認證。</span><span class="sxs-lookup"><span data-stu-id="21df4-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="21df4-111">服務主體是透過提供物件識別碼或服務主體名稱來識別。</span><span class="sxs-lookup"><span data-stu-id="21df4-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="21df4-112">示例</span><span class="sxs-lookup"><span data-stu-id="21df4-112">EXAMPLES</span></span>

### <span data-ttu-id="21df4-113">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="21df4-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password "P@ssw0rd!"
```

<span data-ttu-id="21df4-114">新的密碼認證已新增至現有的服務主體。</span><span class="sxs-lookup"><span data-stu-id="21df4-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="21df4-115">在這個範例中，會將提供的密碼值新增到使用 objectId 的服務主體。</span><span class="sxs-lookup"><span data-stu-id="21df4-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="21df4-116">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="21df4-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="21df4-117">現有的服務主體會新增新的金鑰認證。</span><span class="sxs-lookup"><span data-stu-id="21df4-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="21df4-118">在這個範例中，提供的 base64 編碼公用 X509 憑證 ( "myapp" ) 是使用其 SPN 新增至服務主體。</span><span class="sxs-lookup"><span data-stu-id="21df4-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="21df4-119">--------------------------範例 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="21df4-119">--------------------------  Example 3  --------------------------</span></span>
<span data-ttu-id="21df4-120">@ {段落 = PS C： \\ \> }</span><span class="sxs-lookup"><span data-stu-id="21df4-120">@{paragraph=PS C:\\\>}</span></span>







```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="21df4-121">參數</span><span class="sxs-lookup"><span data-stu-id="21df4-121">PARAMETERS</span></span>

### <span data-ttu-id="21df4-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="21df4-122">-CertValue</span></span>
<span data-ttu-id="21df4-123">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="21df4-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="21df4-124">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="21df4-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="21df4-125">-結束日期</span><span class="sxs-lookup"><span data-stu-id="21df4-125">-EndDate</span></span>
<span data-ttu-id="21df4-126">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="21df4-126">The effective end date of the credential usage.</span></span>
<span data-ttu-id="21df4-127">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="21df4-127">The default end date value is one year from today.</span></span> <span data-ttu-id="21df4-128">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="21df4-128">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="21df4-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="21df4-129">-ObjectId</span></span>
<span data-ttu-id="21df4-130">要新增認證的服務主體物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="21df4-130">The object id of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="21df4-131">-Password</span><span class="sxs-lookup"><span data-stu-id="21df4-131">-Password</span></span>
<span data-ttu-id="21df4-132">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="21df4-132">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21df4-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="21df4-133">-ServicePrincipalName</span></span>
<span data-ttu-id="21df4-134">要新增認證之服務主體 (SPN) 的名稱。</span><span class="sxs-lookup"><span data-stu-id="21df4-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="21df4-135">-開始日期</span><span class="sxs-lookup"><span data-stu-id="21df4-135">-StartDate</span></span>
<span data-ttu-id="21df4-136">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="21df4-136">The effective start date of the credential usage.</span></span>
<span data-ttu-id="21df4-137">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="21df4-137">The default start date value is today.</span></span> <span data-ttu-id="21df4-138">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="21df4-138">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="21df4-139">-確認</span><span class="sxs-lookup"><span data-stu-id="21df4-139">-Confirm</span></span>
<span data-ttu-id="21df4-140">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21df4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21df4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21df4-141">-WhatIf</span></span>
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

### <span data-ttu-id="21df4-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21df4-142">-DefaultProfile</span></span>
<span data-ttu-id="21df4-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21df4-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21df4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21df4-144">CommonParameters</span></span>
<span data-ttu-id="21df4-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21df4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21df4-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21df4-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21df4-147">輸入</span><span class="sxs-lookup"><span data-stu-id="21df4-147">INPUTS</span></span>

## <span data-ttu-id="21df4-148">輸出</span><span class="sxs-lookup"><span data-stu-id="21df4-148">OUTPUTS</span></span>

### <span data-ttu-id="21df4-149">Microsoft.Azure.Graph.RBAC.Version1_6 PSADCredential</span><span class="sxs-lookup"><span data-stu-id="21df4-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="21df4-150">筆記</span><span class="sxs-lookup"><span data-stu-id="21df4-150">NOTES</span></span>

## <span data-ttu-id="21df4-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="21df4-151">RELATED LINKS</span></span>

[<span data-ttu-id="21df4-152">AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="21df4-152">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="21df4-153">移除-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="21df4-153">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="21df4-154">AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="21df4-154">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



