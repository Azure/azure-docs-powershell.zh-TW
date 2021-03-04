---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: e72729b1721fb31ca2ce3a52d33f0295c55bb537
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914797"
---
# <span data-ttu-id="1dee4-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="1dee4-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="1dee4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="1dee4-102">SYNOPSIS</span></span>
<span data-ttu-id="1dee4-103">建立記憶體內憑證系統管理員詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="1dee4-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="1dee4-104">語法</span><span class="sxs-lookup"><span data-stu-id="1dee4-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dee4-105">描述</span><span class="sxs-lookup"><span data-stu-id="1dee4-105">DESCRIPTION</span></span>
<span data-ttu-id="1dee4-106">**New-AzKeyVaultCertificateAdministratorDetail** Cmdlet 會建立記憶體內憑證系統管理員詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="1dee4-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="1dee4-107">例子</span><span class="sxs-lookup"><span data-stu-id="1dee4-107">EXAMPLES</span></span>

### <span data-ttu-id="1dee4-108">範例 1：建立憑證系統管理員詳細資料物件</span><span class="sxs-lookup"><span data-stu-id="1dee4-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="1dee4-109">此命令會建立記憶體內憑證系統管理員詳細資料物件，然後將它儲存在$AdminDetails變數。</span><span class="sxs-lookup"><span data-stu-id="1dee4-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="1dee4-110">參數</span><span class="sxs-lookup"><span data-stu-id="1dee4-110">PARAMETERS</span></span>

### <span data-ttu-id="1dee4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dee4-111">-DefaultProfile</span></span>
<span data-ttu-id="1dee4-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="1dee4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1dee4-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="1dee4-113">-EmailAddress</span></span>
<span data-ttu-id="1dee4-114">指定憑證系統管理員的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="1dee4-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="1dee4-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="1dee4-115">-FirstName</span></span>
<span data-ttu-id="1dee4-116">指定憑證系統管理員的名字。</span><span class="sxs-lookup"><span data-stu-id="1dee4-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="1dee4-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="1dee4-117">-LastName</span></span>
<span data-ttu-id="1dee4-118">指定憑證系統管理員的姓氏。</span><span class="sxs-lookup"><span data-stu-id="1dee4-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="1dee4-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="1dee4-119">-PhoneNumber</span></span>
<span data-ttu-id="1dee4-120">指定憑證系統管理員的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="1dee4-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="1dee4-121">-確認</span><span class="sxs-lookup"><span data-stu-id="1dee4-121">-Confirm</span></span>
<span data-ttu-id="1dee4-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="1dee4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dee4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dee4-123">-WhatIf</span></span>
<span data-ttu-id="1dee4-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1dee4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dee4-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1dee4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dee4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dee4-126">CommonParameters</span></span>
<span data-ttu-id="1dee4-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="1dee4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dee4-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1dee4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dee4-129">輸入</span><span class="sxs-lookup"><span data-stu-id="1dee4-129">INPUTS</span></span>

### <span data-ttu-id="1dee4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1dee4-130">System.String</span></span>

## <span data-ttu-id="1dee4-131">輸出</span><span class="sxs-lookup"><span data-stu-id="1dee4-131">OUTPUTS</span></span>

### <span data-ttu-id="1dee4-132">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="1dee4-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="1dee4-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1dee4-133">NOTES</span></span>

## <span data-ttu-id="1dee4-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dee4-134">RELATED LINKS</span></span>

[<span data-ttu-id="1dee4-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="1dee4-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

