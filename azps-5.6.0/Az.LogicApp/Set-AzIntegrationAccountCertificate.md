---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: c7ae1404cfff2d725326b9f5a8f2b7244c030109
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913522"
---
# <span data-ttu-id="1dafd-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1dafd-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="1dafd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1dafd-102">SYNOPSIS</span></span>
<span data-ttu-id="1dafd-103">修改整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="1dafd-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="1dafd-104">語法</span><span class="sxs-lookup"><span data-stu-id="1dafd-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1dafd-105">描述</span><span class="sxs-lookup"><span data-stu-id="1dafd-105">DESCRIPTION</span></span>
<span data-ttu-id="1dafd-106">**Set-AzIficAccountCertificate** Cmdlet 會修改整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="1dafd-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="1dafd-107">此 Cmdlet 會返回代表整合帳戶憑證的物件。</span><span class="sxs-lookup"><span data-stu-id="1dafd-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="1dafd-108">指定整合帳戶名稱、資源組名和憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="1dafd-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="1dafd-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="1dafd-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1dafd-110">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="1dafd-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1dafd-111">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="1dafd-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1dafd-112">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="1dafd-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1dafd-113">例子</span><span class="sxs-lookup"><span data-stu-id="1dafd-113">EXAMPLES</span></span>

### <span data-ttu-id="1dafd-114">範例 1：修改整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="1dafd-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="1dafd-115">此命令會修改指定資源群組中的整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="1dafd-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="1dafd-116">參數</span><span class="sxs-lookup"><span data-stu-id="1dafd-116">PARAMETERS</span></span>

### <span data-ttu-id="1dafd-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="1dafd-117">-CertificateName</span></span>
<span data-ttu-id="1dafd-118">指定整合帳戶憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dafd-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="1dafd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dafd-119">-DefaultProfile</span></span>
<span data-ttu-id="1dafd-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1dafd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dafd-121">-強制</span><span class="sxs-lookup"><span data-stu-id="1dafd-121">-Force</span></span>
<span data-ttu-id="1dafd-122">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1dafd-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dafd-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1dafd-123">-KeyName</span></span>
<span data-ttu-id="1dafd-124">指定金鑰庫中憑證金鑰的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dafd-124">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="1dafd-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="1dafd-125">-KeyVaultId</span></span>
<span data-ttu-id="1dafd-126">指定金鑰庫識別碼。</span><span class="sxs-lookup"><span data-stu-id="1dafd-126">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="1dafd-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="1dafd-127">-KeyVersion</span></span>
<span data-ttu-id="1dafd-128">指定金鑰庫中憑證金鑰的版本。</span><span class="sxs-lookup"><span data-stu-id="1dafd-128">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="1dafd-129">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="1dafd-129">-Metadata</span></span>
<span data-ttu-id="1dafd-130">指定憑證的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="1dafd-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="1dafd-131">-名稱</span><span class="sxs-lookup"><span data-stu-id="1dafd-131">-Name</span></span>
<span data-ttu-id="1dafd-132">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dafd-132">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dafd-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="1dafd-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="1dafd-134">指定公用憑證的路徑 (.cer) 檔案。</span><span class="sxs-lookup"><span data-stu-id="1dafd-134">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="1dafd-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dafd-135">-ResourceGroupName</span></span>
<span data-ttu-id="1dafd-136">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dafd-136">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1dafd-137">-確認</span><span class="sxs-lookup"><span data-stu-id="1dafd-137">-Confirm</span></span>
<span data-ttu-id="1dafd-138">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1dafd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dafd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dafd-139">-WhatIf</span></span>
<span data-ttu-id="1dafd-140">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1dafd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dafd-141">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dafd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dafd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dafd-142">CommonParameters</span></span>
<span data-ttu-id="1dafd-143">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1dafd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dafd-144">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="1dafd-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dafd-145">輸入</span><span class="sxs-lookup"><span data-stu-id="1dafd-145">INPUTS</span></span>

### <span data-ttu-id="1dafd-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1dafd-146">System.String</span></span>

## <span data-ttu-id="1dafd-147">輸出</span><span class="sxs-lookup"><span data-stu-id="1dafd-147">OUTPUTS</span></span>

### <span data-ttu-id="1dafd-148">Microsoft.Azure.management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1dafd-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="1dafd-149">筆記</span><span class="sxs-lookup"><span data-stu-id="1dafd-149">NOTES</span></span>

## <span data-ttu-id="1dafd-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dafd-150">RELATED LINKS</span></span>

[<span data-ttu-id="1dafd-151">Get-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1dafd-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="1dafd-152">New-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1dafd-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="1dafd-153">Remove-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="1dafd-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


