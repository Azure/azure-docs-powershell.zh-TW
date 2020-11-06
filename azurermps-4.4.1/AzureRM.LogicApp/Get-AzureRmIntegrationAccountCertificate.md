---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C0086E73-CCB1-4B75-B367-C79E17738122
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 3d26bca20befc31edfa437c7d3f9bc5dfced2b7b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446779"
---
# <span data-ttu-id="4f25e-101">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4f25e-101">Get-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="4f25e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f25e-102">SYNOPSIS</span></span>
<span data-ttu-id="4f25e-103">從資源群組取得整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="4f25e-103">Gets integration account certificates from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f25e-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f25e-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCertificate [-ResourceGroupName <String>] [-Name <String>]
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f25e-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f25e-105">DESCRIPTION</span></span>
<span data-ttu-id="4f25e-106">**AzureRmIntegrationAccountCertificate** Cmdlet 會從資源群組取得整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="4f25e-106">The **Get-AzureRmIntegrationAccountCertificate** cmdlet gets integration account certificates from a resource group.</span></span>
<span data-ttu-id="4f25e-107">指定整合帳戶名稱、資源群組名稱及憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="4f25e-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="4f25e-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="4f25e-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4f25e-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="4f25e-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4f25e-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="4f25e-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4f25e-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="4f25e-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4f25e-112">示例</span><span class="sxs-lookup"><span data-stu-id="4f25e-112">EXAMPLES</span></span>

### <span data-ttu-id="4f25e-113">範例1：取得整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="4f25e-113">Example 1: Get an integration account certificate</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="4f25e-114">這個命令會取得名為 IntegrationAccountCertificate01 的整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="4f25e-114">This command gets the integration account certificate named IntegrationAccountCertificate01.</span></span>

### <span data-ttu-id="4f25e-115">範例2：依整合帳戶名稱取得整合帳戶憑證</span><span class="sxs-lookup"><span data-stu-id="4f25e-115">Example 2: Get integration account certificates by integration account name</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
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

<span data-ttu-id="4f25e-116">這個命令會取得名為 IntegrationAccount31 之整合帳戶的整合帳戶憑證。</span><span class="sxs-lookup"><span data-stu-id="4f25e-116">This command gets the integration account certificates for the  integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="4f25e-117">參數</span><span class="sxs-lookup"><span data-stu-id="4f25e-117">PARAMETERS</span></span>

### <span data-ttu-id="4f25e-118">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4f25e-118">-CertificateName</span></span>
<span data-ttu-id="4f25e-119">指定整合帳戶憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f25e-119">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="4f25e-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f25e-120">-Name</span></span>
<span data-ttu-id="4f25e-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f25e-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="4f25e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f25e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f25e-123">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f25e-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4f25e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f25e-124">-DefaultProfile</span></span>
<span data-ttu-id="4f25e-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4f25e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f25e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f25e-126">CommonParameters</span></span>
<span data-ttu-id="4f25e-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f25e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f25e-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f25e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f25e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4f25e-129">INPUTS</span></span>

## <span data-ttu-id="4f25e-130">輸出</span><span class="sxs-lookup"><span data-stu-id="4f25e-130">OUTPUTS</span></span>

### <span data-ttu-id="4f25e-131">IntegrationAccountCertificate 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="4f25e-131">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="4f25e-132">筆記</span><span class="sxs-lookup"><span data-stu-id="4f25e-132">NOTES</span></span>

## <span data-ttu-id="4f25e-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f25e-133">RELATED LINKS</span></span>

[<span data-ttu-id="4f25e-134">新-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4f25e-134">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="4f25e-135">移除-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4f25e-135">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="4f25e-136">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="4f25e-136">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


