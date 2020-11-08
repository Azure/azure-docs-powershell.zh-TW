---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140108"
---
# <span data-ttu-id="feb3f-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="feb3f-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="feb3f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="feb3f-102">SYNOPSIS</span></span>
<span data-ttu-id="feb3f-103">建立記憶體內部的憑證系統管理員詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="feb3f-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="feb3f-104">句法</span><span class="sxs-lookup"><span data-stu-id="feb3f-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feb3f-105">說明</span><span class="sxs-lookup"><span data-stu-id="feb3f-105">DESCRIPTION</span></span>
<span data-ttu-id="feb3f-106">**新的-AzKeyVaultCertificateAdministratorDetail** Cmdlet 會建立記憶體中的憑證系統管理員詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="feb3f-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="feb3f-107">示例</span><span class="sxs-lookup"><span data-stu-id="feb3f-107">EXAMPLES</span></span>

### <span data-ttu-id="feb3f-108">範例1：建立憑證管理員詳細資料物件</span><span class="sxs-lookup"><span data-stu-id="feb3f-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="feb3f-109">這個命令會建立記憶體內部的憑證系統管理員詳細資料物件，然後將它儲存在 $AdminDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="feb3f-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="feb3f-110">參數</span><span class="sxs-lookup"><span data-stu-id="feb3f-110">PARAMETERS</span></span>

### <span data-ttu-id="feb3f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feb3f-111">-DefaultProfile</span></span>
<span data-ttu-id="feb3f-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="feb3f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="feb3f-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="feb3f-113">-EmailAddress</span></span>
<span data-ttu-id="feb3f-114">指定憑證管理員的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="feb3f-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="feb3f-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="feb3f-115">-FirstName</span></span>
<span data-ttu-id="feb3f-116">指定憑證管理員的第一個名稱。</span><span class="sxs-lookup"><span data-stu-id="feb3f-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="feb3f-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="feb3f-117">-LastName</span></span>
<span data-ttu-id="feb3f-118">指定憑證管理員的姓氏。</span><span class="sxs-lookup"><span data-stu-id="feb3f-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="feb3f-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="feb3f-119">-PhoneNumber</span></span>
<span data-ttu-id="feb3f-120">指定憑證管理員的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="feb3f-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="feb3f-121">-確認</span><span class="sxs-lookup"><span data-stu-id="feb3f-121">-Confirm</span></span>
<span data-ttu-id="feb3f-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="feb3f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feb3f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feb3f-123">-WhatIf</span></span>
<span data-ttu-id="feb3f-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="feb3f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="feb3f-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="feb3f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feb3f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feb3f-126">CommonParameters</span></span>
<span data-ttu-id="feb3f-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="feb3f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feb3f-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="feb3f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feb3f-129">輸入</span><span class="sxs-lookup"><span data-stu-id="feb3f-129">INPUTS</span></span>

### <span data-ttu-id="feb3f-130">System.object</span><span class="sxs-lookup"><span data-stu-id="feb3f-130">System.String</span></span>

## <span data-ttu-id="feb3f-131">輸出</span><span class="sxs-lookup"><span data-stu-id="feb3f-131">OUTPUTS</span></span>

### <span data-ttu-id="feb3f-132">PSKeyVaultCertificateAdministratorDetails 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="feb3f-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="feb3f-133">筆記</span><span class="sxs-lookup"><span data-stu-id="feb3f-133">NOTES</span></span>

## <span data-ttu-id="feb3f-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="feb3f-134">RELATED LINKS</span></span>

[<span data-ttu-id="feb3f-135">新-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="feb3f-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

