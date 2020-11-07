---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: d4d7cb0a188b4c00c4ea0c07140b3360c98805aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624674"
---
# <span data-ttu-id="eb968-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="eb968-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="eb968-102">摘要</span><span class="sxs-lookup"><span data-stu-id="eb968-102">SYNOPSIS</span></span>
<span data-ttu-id="eb968-103">在現有的應用程式中新增認證。</span><span class="sxs-lookup"><span data-stu-id="eb968-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb968-104">句法</span><span class="sxs-lookup"><span data-stu-id="eb968-104">SYNTAX</span></span>

### <span data-ttu-id="eb968-105">ApplicationObjectIdWithPasswordParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="eb968-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb968-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb968-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb968-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb968-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb968-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb968-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb968-109">說明</span><span class="sxs-lookup"><span data-stu-id="eb968-109">DESCRIPTION</span></span>
<span data-ttu-id="eb968-110">New-AzureRmADAppCredential Cmdlet 可以用來新增認證或為應用程式轉移認證。</span><span class="sxs-lookup"><span data-stu-id="eb968-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="eb968-111">應用程式是透過提供應用程式物件識別碼或應用程式識別碼來識別。</span><span class="sxs-lookup"><span data-stu-id="eb968-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="eb968-112">示例</span><span class="sxs-lookup"><span data-stu-id="eb968-112">EXAMPLES</span></span>

### <span data-ttu-id="eb968-113">範例1</span><span class="sxs-lookup"><span data-stu-id="eb968-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="eb968-114">新的密碼認證已新增至現有的應用程式。</span><span class="sxs-lookup"><span data-stu-id="eb968-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="eb968-115">在這個範例中，提供的密碼值會使用 application 物件識別碼新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="eb968-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="eb968-116">範例2</span><span class="sxs-lookup"><span data-stu-id="eb968-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="eb968-117">現有的應用程式會新增一個新的金鑰認證。</span><span class="sxs-lookup"><span data-stu-id="eb968-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="eb968-118">在這個範例中，提供的 base64 編碼公用 X509 憑證 ( "myapp" ) 是使用 applicationId 新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="eb968-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="eb968-119">範例3</span><span class="sxs-lookup"><span data-stu-id="eb968-119">Example 3</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="eb968-120">參數</span><span class="sxs-lookup"><span data-stu-id="eb968-120">PARAMETERS</span></span>

### <span data-ttu-id="eb968-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="eb968-121">-ApplicationId</span></span>
<span data-ttu-id="eb968-122">要新增認證的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb968-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb968-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="eb968-123">-CertValue</span></span>
<span data-ttu-id="eb968-124">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="eb968-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="eb968-125">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="eb968-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb968-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb968-126">-DefaultProfile</span></span>
<span data-ttu-id="eb968-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="eb968-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb968-128">-結束日期</span><span class="sxs-lookup"><span data-stu-id="eb968-128">-EndDate</span></span>
<span data-ttu-id="eb968-129">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="eb968-129">The effective end date of the credential usage.</span></span>
<span data-ttu-id="eb968-130">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="eb968-130">The default end date value is one year from today.</span></span> <span data-ttu-id="eb968-131">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="eb968-131">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="eb968-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="eb968-132">-ObjectId</span></span>
<span data-ttu-id="eb968-133">要新增認證之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb968-133">The object id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb968-134">-Password</span><span class="sxs-lookup"><span data-stu-id="eb968-134">-Password</span></span>
<span data-ttu-id="eb968-135">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="eb968-135">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb968-136">-開始日期</span><span class="sxs-lookup"><span data-stu-id="eb968-136">-StartDate</span></span>
<span data-ttu-id="eb968-137">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="eb968-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="eb968-138">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="eb968-138">The default start date value is today.</span></span>
<span data-ttu-id="eb968-139">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="eb968-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="eb968-140">-確認</span><span class="sxs-lookup"><span data-stu-id="eb968-140">-Confirm</span></span>
<span data-ttu-id="eb968-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="eb968-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb968-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb968-142">-WhatIf</span></span>
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

### <span data-ttu-id="eb968-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb968-143">CommonParameters</span></span>
<span data-ttu-id="eb968-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="eb968-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb968-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="eb968-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb968-146">輸入</span><span class="sxs-lookup"><span data-stu-id="eb968-146">INPUTS</span></span>

### <span data-ttu-id="eb968-147">所有</span><span class="sxs-lookup"><span data-stu-id="eb968-147">None</span></span>
<span data-ttu-id="eb968-148">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="eb968-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eb968-149">輸出</span><span class="sxs-lookup"><span data-stu-id="eb968-149">OUTPUTS</span></span>

### <span data-ttu-id="eb968-150">Microsoft.Azure.Graph.RBAC.Version1_6 PSADCredential</span><span class="sxs-lookup"><span data-stu-id="eb968-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="eb968-151">筆記</span><span class="sxs-lookup"><span data-stu-id="eb968-151">NOTES</span></span>

## <span data-ttu-id="eb968-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="eb968-152">RELATED LINKS</span></span>

[<span data-ttu-id="eb968-153">AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="eb968-153">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="eb968-154">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="eb968-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="eb968-155">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="eb968-155">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

