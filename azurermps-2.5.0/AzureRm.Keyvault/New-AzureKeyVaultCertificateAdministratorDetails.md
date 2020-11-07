---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
ms.openlocfilehash: 50da8cae0af437ee86fd7462b285b812368b2508
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801646"
---
# <span data-ttu-id="a304d-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="a304d-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="a304d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a304d-102">SYNOPSIS</span></span>
<span data-ttu-id="a304d-103">建立記憶體內部的憑證系統管理員詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="a304d-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a304d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a304d-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a304d-105">說明</span><span class="sxs-lookup"><span data-stu-id="a304d-105">DESCRIPTION</span></span>
<span data-ttu-id="a304d-106">**新的-AzureKeyVaultCertificateAdministratorDetails** Cmdlet 會建立記憶體中的憑證系統管理員詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="a304d-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="a304d-107">示例</span><span class="sxs-lookup"><span data-stu-id="a304d-107">EXAMPLES</span></span>

### <span data-ttu-id="a304d-108">範例1：建立憑證管理員詳細資料物件</span><span class="sxs-lookup"><span data-stu-id="a304d-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="a304d-109">這個命令會建立記憶體內部的憑證系統管理員詳細資料物件，然後將它儲存在 $AdminDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="a304d-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="a304d-110">參數</span><span class="sxs-lookup"><span data-stu-id="a304d-110">PARAMETERS</span></span>

### <span data-ttu-id="a304d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a304d-111">-DefaultProfile</span></span>
<span data-ttu-id="a304d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a304d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a304d-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a304d-113">-EmailAddress</span></span>
<span data-ttu-id="a304d-114">指定憑證管理員的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="a304d-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="a304d-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="a304d-115">-FirstName</span></span>
<span data-ttu-id="a304d-116">指定憑證管理員的第一個名稱。</span><span class="sxs-lookup"><span data-stu-id="a304d-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="a304d-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="a304d-117">-LastName</span></span>
<span data-ttu-id="a304d-118">指定憑證管理員的姓氏。</span><span class="sxs-lookup"><span data-stu-id="a304d-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="a304d-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="a304d-119">-PhoneNumber</span></span>
<span data-ttu-id="a304d-120">指定憑證管理員的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="a304d-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="a304d-121">-確認</span><span class="sxs-lookup"><span data-stu-id="a304d-121">-Confirm</span></span>
<span data-ttu-id="a304d-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a304d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a304d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a304d-123">-WhatIf</span></span>
<span data-ttu-id="a304d-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a304d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a304d-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a304d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a304d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a304d-126">CommonParameters</span></span>
<span data-ttu-id="a304d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a304d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a304d-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a304d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a304d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="a304d-129">INPUTS</span></span>

## <span data-ttu-id="a304d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="a304d-130">OUTPUTS</span></span>

### <span data-ttu-id="a304d-131">KeyVaultCertificateAdministratorDetails 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="a304d-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="a304d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="a304d-132">NOTES</span></span>

## <span data-ttu-id="a304d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="a304d-133">RELATED LINKS</span></span>

[<span data-ttu-id="a304d-134">新-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="a304d-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

