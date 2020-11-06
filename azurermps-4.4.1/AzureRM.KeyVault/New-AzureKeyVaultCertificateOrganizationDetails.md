---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: e607181b1f44508078f82b25e23e9d1fe53158db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446788"
---
# <span data-ttu-id="81d69-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="81d69-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="81d69-102">摘要</span><span class="sxs-lookup"><span data-stu-id="81d69-102">SYNOPSIS</span></span>
<span data-ttu-id="81d69-103">建立記憶體內部的憑證組織詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="81d69-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="81d69-104">句法</span><span class="sxs-lookup"><span data-stu-id="81d69-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81d69-105">說明</span><span class="sxs-lookup"><span data-stu-id="81d69-105">DESCRIPTION</span></span>
<span data-ttu-id="81d69-106">**新的-AzureKeyVaultCertificateOrganizationDetails** Cmdlet 會建立記憶體內部的憑證組織詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="81d69-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="81d69-107">示例</span><span class="sxs-lookup"><span data-stu-id="81d69-107">EXAMPLES</span></span>

### <span data-ttu-id="81d69-108">範例1：建立組織詳細資料物件</span><span class="sxs-lookup"><span data-stu-id="81d69-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="81d69-109">第一個命令會建立憑證管理員詳細資料物件，然後將它儲存在 $AdminDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="81d69-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="81d69-110">第二個命令會建立憑證組織詳細資料物件，然後將其儲存在 $OrgDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="81d69-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="81d69-111">參數</span><span class="sxs-lookup"><span data-stu-id="81d69-111">PARAMETERS</span></span>

### <span data-ttu-id="81d69-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="81d69-112">-AdministratorDetails</span></span>
<span data-ttu-id="81d69-113">指定 [證書組織管理員]。</span><span class="sxs-lookup"><span data-stu-id="81d69-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="81d69-114">-識別碼</span><span class="sxs-lookup"><span data-stu-id="81d69-114">-Id</span></span>
<span data-ttu-id="81d69-115">指定組織的識別碼。</span><span class="sxs-lookup"><span data-stu-id="81d69-115">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="81d69-116">-確認</span><span class="sxs-lookup"><span data-stu-id="81d69-116">-Confirm</span></span>
<span data-ttu-id="81d69-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="81d69-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81d69-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81d69-118">-WhatIf</span></span>
<span data-ttu-id="81d69-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="81d69-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81d69-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="81d69-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81d69-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d69-121">-DefaultProfile</span></span>
<span data-ttu-id="81d69-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="81d69-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d69-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d69-123">CommonParameters</span></span>
<span data-ttu-id="81d69-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="81d69-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d69-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="81d69-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d69-126">輸入</span><span class="sxs-lookup"><span data-stu-id="81d69-126">INPUTS</span></span>

## <span data-ttu-id="81d69-127">輸出</span><span class="sxs-lookup"><span data-stu-id="81d69-127">OUTPUTS</span></span>

### <span data-ttu-id="81d69-128">KeyVaultCertificateOrganizationDetails 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="81d69-128">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="81d69-129">筆記</span><span class="sxs-lookup"><span data-stu-id="81d69-129">NOTES</span></span>

## <span data-ttu-id="81d69-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="81d69-130">RELATED LINKS</span></span>

[<span data-ttu-id="81d69-131">新-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="81d69-131">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

