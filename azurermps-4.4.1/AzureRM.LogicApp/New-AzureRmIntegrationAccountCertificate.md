---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 93136177289d169771dd1ba00ba875f2e7c06c45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623664"
---
# <span data-ttu-id="4b33d-101">New-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4b33d-101">New-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="4b33d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4b33d-102">SYNOPSIS</span></span>
<span data-ttu-id="4b33d-103">建立整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="4b33d-103">Creates an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b33d-104">句法</span><span class="sxs-lookup"><span data-stu-id="4b33d-104">SYNTAX</span></span>

### <span data-ttu-id="4b33d-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="4b33d-105">PrivateKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b33d-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="4b33d-106">PublicKey</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b33d-107">同時</span><span class="sxs-lookup"><span data-stu-id="4b33d-107">Both</span></span>
```
New-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b33d-108">說明</span><span class="sxs-lookup"><span data-stu-id="4b33d-108">DESCRIPTION</span></span>
<span data-ttu-id="4b33d-109">**新的-AzureRmIntegrationAccountCertificate** Cmdlet 會建立整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="4b33d-109">The **New-AzureRmIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="4b33d-110">這個 Cmdlet 會傳回代表整合帳戶憑證的物件。</span><span class="sxs-lookup"><span data-stu-id="4b33d-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="4b33d-111">指定整合帳戶名稱、資源組名稱、憑證名稱、金鑰名稱、金鑰版本及金鑰 vault ID。</span><span class="sxs-lookup"><span data-stu-id="4b33d-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="4b33d-112">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="4b33d-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="4b33d-113">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="4b33d-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4b33d-114">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="4b33d-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4b33d-115">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="4b33d-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4b33d-116">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="4b33d-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4b33d-117">示例</span><span class="sxs-lookup"><span data-stu-id="4b33d-117">EXAMPLES</span></span>

### <span data-ttu-id="4b33d-118">範例1：建立整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="4b33d-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="4b33d-119">這個命令會在指定的資源群組中建立整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="4b33d-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="4b33d-120">參數</span><span class="sxs-lookup"><span data-stu-id="4b33d-120">PARAMETERS</span></span>

### <span data-ttu-id="4b33d-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4b33d-121">-CertificateName</span></span>
<span data-ttu-id="4b33d-122">指定整合帳戶憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b33d-122">Specifies a name for the integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b33d-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="4b33d-123">-KeyName</span></span>
<span data-ttu-id="4b33d-124">指定 [主要電子倉庫] 中憑證金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b33d-124">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b33d-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="4b33d-125">-KeyVaultId</span></span>
<span data-ttu-id="4b33d-126">指定金鑰 vault ID。</span><span class="sxs-lookup"><span data-stu-id="4b33d-126">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b33d-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="4b33d-127">-KeyVersion</span></span>
<span data-ttu-id="4b33d-128">指定 [金鑰 vault] 中的憑證金鑰版本。</span><span class="sxs-lookup"><span data-stu-id="4b33d-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b33d-129">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="4b33d-129">-Metadata</span></span>
<span data-ttu-id="4b33d-130">指定憑證的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="4b33d-130">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b33d-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="4b33d-131">-Name</span></span>
<span data-ttu-id="4b33d-132">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b33d-132">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b33d-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4b33d-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="4b33d-134">指定公用憑證 ( .cer) 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="4b33d-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b33d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b33d-135">-ResourceGroupName</span></span>
<span data-ttu-id="4b33d-136">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4b33d-136">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b33d-137">-確認</span><span class="sxs-lookup"><span data-stu-id="4b33d-137">-Confirm</span></span>
<span data-ttu-id="4b33d-138">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4b33d-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b33d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b33d-139">-WhatIf</span></span>
<span data-ttu-id="4b33d-140">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4b33d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b33d-141">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4b33d-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b33d-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b33d-142">-DefaultProfile</span></span>
<span data-ttu-id="4b33d-143">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4b33d-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b33d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b33d-144">CommonParameters</span></span>
<span data-ttu-id="4b33d-145">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4b33d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b33d-146">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4b33d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b33d-147">輸入</span><span class="sxs-lookup"><span data-stu-id="4b33d-147">INPUTS</span></span>

## <span data-ttu-id="4b33d-148">輸出</span><span class="sxs-lookup"><span data-stu-id="4b33d-148">OUTPUTS</span></span>

### <span data-ttu-id="4b33d-149">IntegrationAccountCertificate 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="4b33d-149">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="4b33d-150">筆記</span><span class="sxs-lookup"><span data-stu-id="4b33d-150">NOTES</span></span>

## <span data-ttu-id="4b33d-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="4b33d-151">RELATED LINKS</span></span>

[<span data-ttu-id="4b33d-152">AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4b33d-152">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="4b33d-153">移除-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4b33d-153">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="4b33d-154">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4b33d-154">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


