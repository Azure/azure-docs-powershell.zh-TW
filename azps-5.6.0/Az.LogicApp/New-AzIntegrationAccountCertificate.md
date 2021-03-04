---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 8b1da3fda8c8c016dd9cbe039015553f9073a4b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916527"
---
# <span data-ttu-id="532f0-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="532f0-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="532f0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="532f0-102">SYNOPSIS</span></span>
<span data-ttu-id="532f0-103">建立整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="532f0-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="532f0-104">語法</span><span class="sxs-lookup"><span data-stu-id="532f0-104">SYNTAX</span></span>

### <span data-ttu-id="532f0-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="532f0-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="532f0-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="532f0-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="532f0-107">兩者</span><span class="sxs-lookup"><span data-stu-id="532f0-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="532f0-108">描述</span><span class="sxs-lookup"><span data-stu-id="532f0-108">DESCRIPTION</span></span>
<span data-ttu-id="532f0-109">**New-AzIficAccountCertificate** Cmdlet 會建立整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="532f0-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="532f0-110">此 Cmdlet 會返回代表整合帳戶憑證的物件。</span><span class="sxs-lookup"><span data-stu-id="532f0-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="532f0-111">指定整合帳戶名稱、資源組名、憑證名稱、金鑰名稱、金鑰版本和金鑰庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="532f0-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="532f0-112">在命令列中指定的範本參數檔案值優先于範本參數物件的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="532f0-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="532f0-113">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="532f0-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="532f0-114">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="532f0-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="532f0-115">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="532f0-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="532f0-116">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="532f0-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="532f0-117">例子</span><span class="sxs-lookup"><span data-stu-id="532f0-117">EXAMPLES</span></span>

### <span data-ttu-id="532f0-118">範例 1：建立整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="532f0-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="532f0-119">此命令會建立指定資源群組中的整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="532f0-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="532f0-120">參數</span><span class="sxs-lookup"><span data-stu-id="532f0-120">PARAMETERS</span></span>

### <span data-ttu-id="532f0-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="532f0-121">-CertificateName</span></span>
<span data-ttu-id="532f0-122">指定整合帳戶憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="532f0-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="532f0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="532f0-123">-DefaultProfile</span></span>
<span data-ttu-id="532f0-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="532f0-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="532f0-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="532f0-125">-KeyName</span></span>
<span data-ttu-id="532f0-126">指定金鑰庫中憑證金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="532f0-126">Specifies the name of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="532f0-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="532f0-127">-KeyVaultId</span></span>
<span data-ttu-id="532f0-128">指定金鑰庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="532f0-128">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="532f0-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="532f0-129">-KeyVersion</span></span>
<span data-ttu-id="532f0-130">指定金鑰庫中憑證金鑰的版本。</span><span class="sxs-lookup"><span data-stu-id="532f0-130">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="532f0-131">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="532f0-131">-Metadata</span></span>
<span data-ttu-id="532f0-132">指定憑證的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="532f0-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="532f0-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="532f0-133">-Name</span></span>
<span data-ttu-id="532f0-134">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="532f0-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="532f0-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="532f0-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="532f0-136">指定公用憑證的路徑 (.cer) 檔案。</span><span class="sxs-lookup"><span data-stu-id="532f0-136">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="532f0-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="532f0-137">-ResourceGroupName</span></span>
<span data-ttu-id="532f0-138">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="532f0-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="532f0-139">-確認</span><span class="sxs-lookup"><span data-stu-id="532f0-139">-Confirm</span></span>
<span data-ttu-id="532f0-140">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="532f0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="532f0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="532f0-141">-WhatIf</span></span>
<span data-ttu-id="532f0-142">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="532f0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="532f0-143">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="532f0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="532f0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="532f0-144">CommonParameters</span></span>
<span data-ttu-id="532f0-145">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="532f0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="532f0-146">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="532f0-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="532f0-147">輸入</span><span class="sxs-lookup"><span data-stu-id="532f0-147">INPUTS</span></span>

### <span data-ttu-id="532f0-148">System.String</span><span class="sxs-lookup"><span data-stu-id="532f0-148">System.String</span></span>

## <span data-ttu-id="532f0-149">輸出</span><span class="sxs-lookup"><span data-stu-id="532f0-149">OUTPUTS</span></span>

### <span data-ttu-id="532f0-150">Microsoft.Azure.management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="532f0-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="532f0-151">筆記</span><span class="sxs-lookup"><span data-stu-id="532f0-151">NOTES</span></span>

## <span data-ttu-id="532f0-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="532f0-152">RELATED LINKS</span></span>

[<span data-ttu-id="532f0-153">Get-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="532f0-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="532f0-154">Remove-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="532f0-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="532f0-155">Set-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="532f0-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


