---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: ee2be43882eb434d8bbc533e0d10722f63427a83
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914790"
---
# <span data-ttu-id="8e51f-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="8e51f-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="8e51f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8e51f-102">SYNOPSIS</span></span>
<span data-ttu-id="8e51f-103">建立記憶體內憑證組織詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="8e51f-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="8e51f-104">語法</span><span class="sxs-lookup"><span data-stu-id="8e51f-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e51f-105">描述</span><span class="sxs-lookup"><span data-stu-id="8e51f-105">DESCRIPTION</span></span>
<span data-ttu-id="8e51f-106">**New-AzKeyVaultCertificateOrganizationDetail** Cmdlet 會建立記憶體內憑證組織詳細資料物件。</span><span class="sxs-lookup"><span data-stu-id="8e51f-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="8e51f-107">例子</span><span class="sxs-lookup"><span data-stu-id="8e51f-107">EXAMPLES</span></span>

### <span data-ttu-id="8e51f-108">範例 1：建立組織詳細資料物件</span><span class="sxs-lookup"><span data-stu-id="8e51f-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="8e51f-109">第一個命令會建立憑證系統管理員詳細資料物件，然後將它儲存在$AdminDetails變數中。</span><span class="sxs-lookup"><span data-stu-id="8e51f-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="8e51f-110">第二個命令會建立憑證組織詳細資料物件，然後將它儲存在$OrgDetails變數中。</span><span class="sxs-lookup"><span data-stu-id="8e51f-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="8e51f-111">參數</span><span class="sxs-lookup"><span data-stu-id="8e51f-111">PARAMETERS</span></span>

### <span data-ttu-id="8e51f-112">-系統管理員詳細</span><span class="sxs-lookup"><span data-stu-id="8e51f-112">-AdministratorDetails</span></span>
<span data-ttu-id="8e51f-113">指定憑證組織的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="8e51f-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="8e51f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e51f-114">-DefaultProfile</span></span>
<span data-ttu-id="8e51f-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="8e51f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e51f-116">-Id</span><span class="sxs-lookup"><span data-stu-id="8e51f-116">-Id</span></span>
<span data-ttu-id="8e51f-117">指定組織的識別碼。</span><span class="sxs-lookup"><span data-stu-id="8e51f-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="8e51f-118">-確認</span><span class="sxs-lookup"><span data-stu-id="8e51f-118">-Confirm</span></span>
<span data-ttu-id="8e51f-119">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8e51f-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e51f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e51f-120">-WhatIf</span></span>
<span data-ttu-id="8e51f-121">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8e51f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e51f-122">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8e51f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e51f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e51f-123">CommonParameters</span></span>
<span data-ttu-id="8e51f-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8e51f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e51f-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e51f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e51f-126">輸入</span><span class="sxs-lookup"><span data-stu-id="8e51f-126">INPUTS</span></span>

### <span data-ttu-id="8e51f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8e51f-127">System.String</span></span>

### <span data-ttu-id="8e51f-128">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8e51f-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8e51f-129">輸出</span><span class="sxs-lookup"><span data-stu-id="8e51f-129">OUTPUTS</span></span>

### <span data-ttu-id="8e51f-130">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="8e51f-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="8e51f-131">筆記</span><span class="sxs-lookup"><span data-stu-id="8e51f-131">NOTES</span></span>

## <span data-ttu-id="8e51f-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="8e51f-132">RELATED LINKS</span></span>

[<span data-ttu-id="8e51f-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="8e51f-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

