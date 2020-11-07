---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 204ee5a7a4d0e5247ae3de239dce650deb4cff0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794660"
---
# <span data-ttu-id="82c61-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="82c61-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="82c61-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82c61-102">SYNOPSIS</span></span>
<span data-ttu-id="82c61-103">從金鑰保存庫刪除憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="82c61-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="82c61-104">句法</span><span class="sxs-lookup"><span data-stu-id="82c61-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82c61-105">說明</span><span class="sxs-lookup"><span data-stu-id="82c61-105">DESCRIPTION</span></span>
<span data-ttu-id="82c61-106">**AzKeyVaultCertificateIssuer** Cmdlet 會從金鑰保存庫刪除憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="82c61-106">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="82c61-107">示例</span><span class="sxs-lookup"><span data-stu-id="82c61-107">EXAMPLES</span></span>

### <span data-ttu-id="82c61-108">範例1：移除憑證頒發者</span><span class="sxs-lookup"><span data-stu-id="82c61-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="82c61-109">這個命令會從 [ContosoKV01] 金鑰保存庫中移除名為 TestIssuer01 的憑證簽發者。</span><span class="sxs-lookup"><span data-stu-id="82c61-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="82c61-110">參數</span><span class="sxs-lookup"><span data-stu-id="82c61-110">PARAMETERS</span></span>

### <span data-ttu-id="82c61-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c61-111">-DefaultProfile</span></span>
<span data-ttu-id="82c61-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="82c61-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82c61-113">-Force</span><span class="sxs-lookup"><span data-stu-id="82c61-113">-Force</span></span>
<span data-ttu-id="82c61-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="82c61-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c61-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="82c61-115">-Name</span></span>
<span data-ttu-id="82c61-116">指定要移除之頒發者的名稱。</span><span class="sxs-lookup"><span data-stu-id="82c61-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c61-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82c61-117">-PassThru</span></span>
<span data-ttu-id="82c61-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="82c61-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82c61-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="82c61-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c61-120">-VaultName</span><span class="sxs-lookup"><span data-stu-id="82c61-120">-VaultName</span></span>
<span data-ttu-id="82c61-121">指定主要電子倉庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="82c61-121">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c61-122">-確認</span><span class="sxs-lookup"><span data-stu-id="82c61-122">-Confirm</span></span>
<span data-ttu-id="82c61-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82c61-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c61-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82c61-124">-WhatIf</span></span>
<span data-ttu-id="82c61-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82c61-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82c61-126">未執行 Cmdlet。顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82c61-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82c61-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82c61-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82c61-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c61-128">CommonParameters</span></span>
<span data-ttu-id="82c61-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82c61-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c61-130">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="82c61-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c61-131">輸入</span><span class="sxs-lookup"><span data-stu-id="82c61-131">INPUTS</span></span>

### <span data-ttu-id="82c61-132">所有</span><span class="sxs-lookup"><span data-stu-id="82c61-132">None</span></span>
<span data-ttu-id="82c61-133">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="82c61-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82c61-134">輸出</span><span class="sxs-lookup"><span data-stu-id="82c61-134">OUTPUTS</span></span>

### <span data-ttu-id="82c61-135">KeyVaultCertificateIssuer 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="82c61-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="82c61-136">筆記</span><span class="sxs-lookup"><span data-stu-id="82c61-136">NOTES</span></span>

## <span data-ttu-id="82c61-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="82c61-137">RELATED LINKS</span></span>

[<span data-ttu-id="82c61-138">AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="82c61-138">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="82c61-139">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="82c61-139">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


