---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: 15b3e3fd90a7bacf87062bc12269ca2853276370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456419"
---
# <span data-ttu-id="54117-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="54117-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="54117-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54117-102">SYNOPSIS</span></span>
<span data-ttu-id="54117-103">在現有的應用程式中新增認證。</span><span class="sxs-lookup"><span data-stu-id="54117-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54117-104">句法</span><span class="sxs-lookup"><span data-stu-id="54117-104">SYNTAX</span></span>

### <span data-ttu-id="54117-105">ApplicationObjectIdWithPasswordParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="54117-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54117-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="54117-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54117-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="54117-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54117-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="54117-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54117-109">說明</span><span class="sxs-lookup"><span data-stu-id="54117-109">DESCRIPTION</span></span>
<span data-ttu-id="54117-110">New-AzureRmADAppCredential Cmdlet 可以用來新增認證或為應用程式轉移認證。</span><span class="sxs-lookup"><span data-stu-id="54117-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="54117-111">應用程式是透過提供應用程式物件識別碼或應用程式識別碼來識別。</span><span class="sxs-lookup"><span data-stu-id="54117-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="54117-112">示例</span><span class="sxs-lookup"><span data-stu-id="54117-112">EXAMPLES</span></span>

### <span data-ttu-id="54117-113">--------------------------範例 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="54117-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password P@ssw0rd!
```

<span data-ttu-id="54117-114">新的密碼認證已新增至現有的應用程式。</span><span class="sxs-lookup"><span data-stu-id="54117-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="54117-115">在這個範例中，提供的密碼值會使用 application 物件識別碼新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="54117-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="54117-116">--------------------------範例 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="54117-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="54117-117">現有的應用程式會新增一個新的金鑰認證。</span><span class="sxs-lookup"><span data-stu-id="54117-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="54117-118">在這個範例中，提供的 base64 編碼公用 X509 憑證 ( "myapp" ) 是使用 applicationId 新增至應用程式。</span><span class="sxs-lookup"><span data-stu-id="54117-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="54117-119">--------------------------範例 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="54117-119">--------------------------  Example 3  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="54117-120">參數</span><span class="sxs-lookup"><span data-stu-id="54117-120">PARAMETERS</span></span>

### <span data-ttu-id="54117-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="54117-121">-ApplicationId</span></span>
<span data-ttu-id="54117-122">要新增認證的應用程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="54117-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54117-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="54117-123">-CertValue</span></span>
<span data-ttu-id="54117-124">"未對稱" 憑證類型的值。</span><span class="sxs-lookup"><span data-stu-id="54117-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="54117-125">它代表基64編碼證書。</span><span class="sxs-lookup"><span data-stu-id="54117-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54117-126">-結束日期</span><span class="sxs-lookup"><span data-stu-id="54117-126">-EndDate</span></span>
<span data-ttu-id="54117-127">認證使用的有效結束日期。</span><span class="sxs-lookup"><span data-stu-id="54117-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="54117-128">從今天開始，預設的結束日期值是一年。</span><span class="sxs-lookup"><span data-stu-id="54117-128">The default end date value is one year from today.</span></span> <span data-ttu-id="54117-129">針對 "不對稱" 類型認證，必須將它設定為 [開啟] 或 [在 X509 憑證有效的日期之前]。</span><span class="sxs-lookup"><span data-stu-id="54117-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="54117-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="54117-130">-ObjectId</span></span>
<span data-ttu-id="54117-131">要新增認證之應用程式的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="54117-131">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54117-132">-Password</span><span class="sxs-lookup"><span data-stu-id="54117-132">-Password</span></span>
<span data-ttu-id="54117-133">要與應用程式相關聯的密碼。</span><span class="sxs-lookup"><span data-stu-id="54117-133">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54117-134">-開始日期</span><span class="sxs-lookup"><span data-stu-id="54117-134">-StartDate</span></span>
<span data-ttu-id="54117-135">認證使用的有效開始日期。</span><span class="sxs-lookup"><span data-stu-id="54117-135">The effective start date of the credential usage.</span></span>
<span data-ttu-id="54117-136">預設的 [開始日期] 值為 [今天]。</span><span class="sxs-lookup"><span data-stu-id="54117-136">The default start date value is today.</span></span>
<span data-ttu-id="54117-137">針對 "不對稱" 類型認證，必須將此設定為 [開啟] 或 [在 X509 憑證有效的日期之後]。</span><span class="sxs-lookup"><span data-stu-id="54117-137">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="54117-138">-確認</span><span class="sxs-lookup"><span data-stu-id="54117-138">-Confirm</span></span>
<span data-ttu-id="54117-139">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54117-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54117-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54117-140">-WhatIf</span></span>
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

### <span data-ttu-id="54117-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54117-141">-DefaultProfile</span></span>
<span data-ttu-id="54117-142">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="54117-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54117-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54117-143">CommonParameters</span></span>
<span data-ttu-id="54117-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54117-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54117-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54117-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54117-146">輸入</span><span class="sxs-lookup"><span data-stu-id="54117-146">INPUTS</span></span>

## <span data-ttu-id="54117-147">輸出</span><span class="sxs-lookup"><span data-stu-id="54117-147">OUTPUTS</span></span>

### <span data-ttu-id="54117-148">Microsoft.Azure.Graph.RBAC.Version1_6 PSADCredential</span><span class="sxs-lookup"><span data-stu-id="54117-148">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="54117-149">筆記</span><span class="sxs-lookup"><span data-stu-id="54117-149">NOTES</span></span>

## <span data-ttu-id="54117-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="54117-150">RELATED LINKS</span></span>

[<span data-ttu-id="54117-151">AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="54117-151">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="54117-152">移除-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="54117-152">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="54117-153">AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="54117-153">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

