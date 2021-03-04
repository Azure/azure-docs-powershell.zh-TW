---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3a85b92b930ef24e4cb613de28f6a66b530222cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902069"
---
# <span data-ttu-id="b13ec-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b13ec-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b13ec-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b13ec-102">SYNOPSIS</span></span>
<span data-ttu-id="b13ec-103">從金鑰庫刪除憑證發行者。</span><span class="sxs-lookup"><span data-stu-id="b13ec-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="b13ec-104">語法</span><span class="sxs-lookup"><span data-stu-id="b13ec-104">SYNTAX</span></span>

### <span data-ttu-id="b13ec-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="b13ec-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b13ec-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="b13ec-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b13ec-107">描述</span><span class="sxs-lookup"><span data-stu-id="b13ec-107">DESCRIPTION</span></span>
<span data-ttu-id="b13ec-108">**Remove-AzKeyVaultCertificateIssuer Cmdlet** 會從金鑰庫刪除憑證發行者。</span><span class="sxs-lookup"><span data-stu-id="b13ec-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="b13ec-109">例子</span><span class="sxs-lookup"><span data-stu-id="b13ec-109">EXAMPLES</span></span>

### <span data-ttu-id="b13ec-110">範例 1：移除憑證發行者</span><span class="sxs-lookup"><span data-stu-id="b13ec-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="b13ec-111">此命令會從 ContosoKV01 金鑰庫移除名為 TestIssuer01 的憑證發行者。</span><span class="sxs-lookup"><span data-stu-id="b13ec-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="b13ec-112">參數</span><span class="sxs-lookup"><span data-stu-id="b13ec-112">PARAMETERS</span></span>

### <span data-ttu-id="b13ec-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13ec-113">-DefaultProfile</span></span>
<span data-ttu-id="b13ec-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b13ec-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b13ec-115">-強制</span><span class="sxs-lookup"><span data-stu-id="b13ec-115">-Force</span></span>
<span data-ttu-id="b13ec-116">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b13ec-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b13ec-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b13ec-117">-InputObject</span></span>
<span data-ttu-id="b13ec-118">憑證發行者物件</span><span class="sxs-lookup"><span data-stu-id="b13ec-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b13ec-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b13ec-119">-Name</span></span>
<span data-ttu-id="b13ec-120">指定要移除的發行者名稱。</span><span class="sxs-lookup"><span data-stu-id="b13ec-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13ec-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b13ec-121">-PassThru</span></span>
<span data-ttu-id="b13ec-122">會返回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="b13ec-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b13ec-123">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b13ec-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b13ec-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b13ec-124">-VaultName</span></span>
<span data-ttu-id="b13ec-125">指定金鑰庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b13ec-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13ec-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b13ec-126">-Confirm</span></span>
<span data-ttu-id="b13ec-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b13ec-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b13ec-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13ec-128">-WhatIf</span></span>
<span data-ttu-id="b13ec-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b13ec-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b13ec-130">不會執行 Cmdlet。顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b13ec-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b13ec-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b13ec-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b13ec-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13ec-132">CommonParameters</span></span>
<span data-ttu-id="b13ec-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b13ec-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13ec-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b13ec-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13ec-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b13ec-135">INPUTS</span></span>

### <span data-ttu-id="b13ec-136">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b13ec-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="b13ec-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b13ec-137">OUTPUTS</span></span>

### <span data-ttu-id="b13ec-138">Microsoft.Azure.Commands.KeyVault.models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b13ec-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b13ec-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b13ec-139">NOTES</span></span>

## <span data-ttu-id="b13ec-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="b13ec-140">RELATED LINKS</span></span>

[<span data-ttu-id="b13ec-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b13ec-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="b13ec-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b13ec-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


