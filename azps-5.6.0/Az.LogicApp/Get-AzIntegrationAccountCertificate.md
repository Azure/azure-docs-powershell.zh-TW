---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountCertificate.md
ms.openlocfilehash: caf016d1e1ad18aee1904e9b69ae9330a5f34557
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904077"
---
# <span data-ttu-id="94097-101">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="94097-101">Get-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="94097-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94097-102">SYNOPSIS</span></span>
<span data-ttu-id="94097-103">從資源群組中獲得整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="94097-103">Gets integration account certificates from a resource group.</span></span>

## <span data-ttu-id="94097-104">語法</span><span class="sxs-lookup"><span data-stu-id="94097-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>] [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94097-105">描述</span><span class="sxs-lookup"><span data-stu-id="94097-105">DESCRIPTION</span></span>
<span data-ttu-id="94097-106">**Get-AzIficAccountCertificate** Cmdlet 會從資源群組取得整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="94097-106">The **Get-AzIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="94097-107">指定整合帳戶名稱、資源組名和憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="94097-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="94097-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="94097-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="94097-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="94097-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="94097-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="94097-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="94097-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="94097-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="94097-112">例子</span><span class="sxs-lookup"><span data-stu-id="94097-112">EXAMPLES</span></span>

### <span data-ttu-id="94097-113">範例 1：取得整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="94097-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="94097-114">此命令會獲得名為 IntegrationAccountCertificate01 的整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="94097-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="94097-115">範例 2：使用整合帳戶名稱取得整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="94097-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="94097-116">此命令會針對名為 IntegrationAccount31 的整合帳戶，獲得整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="94097-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="94097-117">參數</span><span class="sxs-lookup"><span data-stu-id="94097-117">PARAMETERS</span></span>

### <span data-ttu-id="94097-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="94097-118">-CertificateName</span></span>
<span data-ttu-id="94097-119">指定整合帳戶憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="94097-119">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94097-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94097-120">-DefaultProfile</span></span>
<span data-ttu-id="94097-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="94097-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94097-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="94097-122">-Name</span></span>
<span data-ttu-id="94097-123">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="94097-123">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94097-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94097-124">-ResourceGroupName</span></span>
<span data-ttu-id="94097-125">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="94097-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="94097-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94097-126">CommonParameters</span></span>
<span data-ttu-id="94097-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94097-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94097-128">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="94097-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94097-129">輸入</span><span class="sxs-lookup"><span data-stu-id="94097-129">INPUTS</span></span>

### <span data-ttu-id="94097-130">System.String</span><span class="sxs-lookup"><span data-stu-id="94097-130">System.String</span></span>

## <span data-ttu-id="94097-131">輸出</span><span class="sxs-lookup"><span data-stu-id="94097-131">OUTPUTS</span></span>

### <span data-ttu-id="94097-132">Microsoft.Azure.management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="94097-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="94097-133">筆記</span><span class="sxs-lookup"><span data-stu-id="94097-133">NOTES</span></span>

## <span data-ttu-id="94097-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="94097-134">RELATED LINKS</span></span>

[<span data-ttu-id="94097-135">New-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="94097-135">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="94097-136">Remove-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="94097-136">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="94097-137">Set-AzIficAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="94097-137">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


