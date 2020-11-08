---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141659"
---
# <span data-ttu-id="e963b-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="e963b-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="e963b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e963b-102">SYNOPSIS</span></span>
<span data-ttu-id="e963b-103">建立記憶體內部的憑證組織詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="e963b-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="e963b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e963b-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e963b-105">說明</span><span class="sxs-lookup"><span data-stu-id="e963b-105">DESCRIPTION</span></span>
<span data-ttu-id="e963b-106">**新的-AzKeyVaultCertificateOrganizationDetail** Cmdlet 會建立記憶體內部的憑證組織詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="e963b-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="e963b-107">示例</span><span class="sxs-lookup"><span data-stu-id="e963b-107">EXAMPLES</span></span>

### <span data-ttu-id="e963b-108">範例1：建立組織詳細資料物件</span><span class="sxs-lookup"><span data-stu-id="e963b-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="e963b-109">第一個命令會建立憑證管理員詳細資料物件，然後將它儲存在 $AdminDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="e963b-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="e963b-110">第二個命令會建立憑證組織詳細資料物件，然後將其儲存在 $OrgDetails 變數中。</span><span class="sxs-lookup"><span data-stu-id="e963b-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="e963b-111">參數</span><span class="sxs-lookup"><span data-stu-id="e963b-111">PARAMETERS</span></span>

### <span data-ttu-id="e963b-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="e963b-112">-AdministratorDetails</span></span>
<span data-ttu-id="e963b-113">指定 [證書組織管理員]。</span><span class="sxs-lookup"><span data-stu-id="e963b-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e963b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e963b-114">-DefaultProfile</span></span>
<span data-ttu-id="e963b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e963b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e963b-116">-識別碼</span><span class="sxs-lookup"><span data-stu-id="e963b-116">-Id</span></span>
<span data-ttu-id="e963b-117">指定組織的識別碼。</span><span class="sxs-lookup"><span data-stu-id="e963b-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="e963b-118">-確認</span><span class="sxs-lookup"><span data-stu-id="e963b-118">-Confirm</span></span>
<span data-ttu-id="e963b-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e963b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e963b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e963b-120">-WhatIf</span></span>
<span data-ttu-id="e963b-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e963b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e963b-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e963b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e963b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e963b-123">CommonParameters</span></span>
<span data-ttu-id="e963b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e963b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e963b-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e963b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e963b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e963b-126">INPUTS</span></span>

### <span data-ttu-id="e963b-127">System.object</span><span class="sxs-lookup"><span data-stu-id="e963b-127">System.String</span></span>

### <span data-ttu-id="e963b-128">[System.object]. 清單 ' 1 [KeyVault. PSKeyVaultCertificateAdministratorDetails，KeyVault，版本 = 1.0.0.0，Culture = 中性，PublicKeyToken = null]]。）））））</span><span class="sxs-lookup"><span data-stu-id="e963b-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e963b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="e963b-129">OUTPUTS</span></span>

### <span data-ttu-id="e963b-130">PSKeyVaultCertificateOrganizationDetails 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="e963b-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="e963b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e963b-131">NOTES</span></span>

## <span data-ttu-id="e963b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e963b-132">RELATED LINKS</span></span>

[<span data-ttu-id="e963b-133">新-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="e963b-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

