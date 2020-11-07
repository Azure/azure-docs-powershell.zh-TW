---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 76208f8d4c1b8b1b463ea5a0f24a4e34e7a82855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93795545"
---
# <span data-ttu-id="e97f6-101">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="e97f6-101">New-AzKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="e97f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e97f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e97f6-103">建立記憶體內部的憑證組織詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="e97f6-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="e97f6-104">句法</span><span class="sxs-lookup"><span data-stu-id="e97f6-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e97f6-105">說明</span><span class="sxs-lookup"><span data-stu-id="e97f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e97f6-106">**新的-AzKeyVaultCertificateOrganizationDetails** Cmdlet 會建立記憶體內部的憑證組織詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="e97f6-106">The **New-AzKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="e97f6-107">示例</span><span class="sxs-lookup"><span data-stu-id="e97f6-107">EXAMPLES</span></span>

### <span data-ttu-id="e97f6-108">範例1：建立組織詳細資料物件</span><span class="sxs-lookup"><span data-stu-id="e97f6-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="e97f6-109">第一個命令會建立憑證管理員詳細資料物件，然後將它儲存在 $AdminDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="e97f6-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="e97f6-110">第二個命令會建立憑證組織詳細資料物件，然後將其儲存在 $OrgDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="e97f6-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="e97f6-111">參數</span><span class="sxs-lookup"><span data-stu-id="e97f6-111">PARAMETERS</span></span>

### <span data-ttu-id="e97f6-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="e97f6-112">-AdministratorDetails</span></span>
<span data-ttu-id="e97f6-113">指定 [證書組織管理員]。</span><span class="sxs-lookup"><span data-stu-id="e97f6-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e97f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e97f6-114">-DefaultProfile</span></span>
<span data-ttu-id="e97f6-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e97f6-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e97f6-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e97f6-116">-Id</span></span>
<span data-ttu-id="e97f6-117">指定組織的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e97f6-117">Specifies the identifier for the organization.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e97f6-118">-確認</span><span class="sxs-lookup"><span data-stu-id="e97f6-118">-Confirm</span></span>
<span data-ttu-id="e97f6-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e97f6-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e97f6-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e97f6-120">-WhatIf</span></span>
<span data-ttu-id="e97f6-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e97f6-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e97f6-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e97f6-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e97f6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e97f6-123">CommonParameters</span></span>
<span data-ttu-id="e97f6-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e97f6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e97f6-125">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e97f6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e97f6-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e97f6-126">INPUTS</span></span>

### <span data-ttu-id="e97f6-127">所有</span><span class="sxs-lookup"><span data-stu-id="e97f6-127">None</span></span>
<span data-ttu-id="e97f6-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e97f6-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e97f6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e97f6-129">OUTPUTS</span></span>

### <span data-ttu-id="e97f6-130">KeyVaultCertificateOrganizationDetails 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e97f6-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="e97f6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e97f6-131">NOTES</span></span>

## <span data-ttu-id="e97f6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e97f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="e97f6-133">新-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="e97f6-133">New-AzKeyVaultCertificateAdministratorDetails</span></span>](./New-AzKeyVaultCertificateAdministratorDetails.md)

