---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmSecurityDomain.md
ms.openlocfilehash: 10a54afa8a6ef2e37beebd9d6cdcd304b2d13979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284695"
---
# <span data-ttu-id="147fc-101">Backup-AzManagedHsmSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="147fc-101">Backup-AzManagedHsmSecurityDomain</span></span>

## <span data-ttu-id="147fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="147fc-102">SYNOPSIS</span></span>
<span data-ttu-id="147fc-103">備份受管理的 HSM 的安全網域資料以進行還原。</span><span class="sxs-lookup"><span data-stu-id="147fc-103">Backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="147fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="147fc-104">SYNTAX</span></span>

### <span data-ttu-id="147fc-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="147fc-105">ByName (Default)</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="147fc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="147fc-106">ByInputObject</span></span>
```
Backup-AzManagedHsmSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="147fc-107">說明</span><span class="sxs-lookup"><span data-stu-id="147fc-107">DESCRIPTION</span></span>
<span data-ttu-id="147fc-108">這個 Cmdlet 會備份受管理 HSM 的安全網域資料以進行還原。</span><span class="sxs-lookup"><span data-stu-id="147fc-108">This cmdlet backs up the security domain data of a managed HSM for restoring.</span></span>

## <span data-ttu-id="147fc-109">示例</span><span class="sxs-lookup"><span data-stu-id="147fc-109">EXAMPLES</span></span>

### <span data-ttu-id="147fc-110">範例1</span><span class="sxs-lookup"><span data-stu-id="147fc-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="147fc-111">這個命令會檢索名為 testmhsm 的受管理 HSM，並將該受管理的 HSM 安全網域的備份儲存到指定的輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="147fc-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="147fc-112">參數</span><span class="sxs-lookup"><span data-stu-id="147fc-112">PARAMETERS</span></span>

### <span data-ttu-id="147fc-113">-憑證</span><span class="sxs-lookup"><span data-stu-id="147fc-113">-Certificates</span></span>
<span data-ttu-id="147fc-114">用來加密安全網域資料之憑證的路徑。</span><span class="sxs-lookup"><span data-stu-id="147fc-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="147fc-115">-DefaultProfile</span></span>
<span data-ttu-id="147fc-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="147fc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="147fc-117">-Force</span><span class="sxs-lookup"><span data-stu-id="147fc-117">-Force</span></span>
<span data-ttu-id="147fc-118">指定是否要覆寫現有的檔案。</span><span class="sxs-lookup"><span data-stu-id="147fc-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="147fc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="147fc-119">-InputObject</span></span>
<span data-ttu-id="147fc-120">代表受管理的 HSM 的物件。</span><span class="sxs-lookup"><span data-stu-id="147fc-120">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="147fc-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="147fc-121">-Name</span></span>
<span data-ttu-id="147fc-122">受管理的 HSM 的名稱。</span><span class="sxs-lookup"><span data-stu-id="147fc-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fc-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="147fc-123">-OutputPath</span></span>
<span data-ttu-id="147fc-124">指定要將安全網域資料下載到哪個路徑。</span><span class="sxs-lookup"><span data-stu-id="147fc-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="147fc-125">-PassThru</span></span>
<span data-ttu-id="147fc-126">在指定時，會在 Cmdlet 成功時傳回布林值。</span><span class="sxs-lookup"><span data-stu-id="147fc-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="147fc-127">-仲裁</span><span class="sxs-lookup"><span data-stu-id="147fc-127">-Quorum</span></span>
<span data-ttu-id="147fc-128">解密安全網域以進行復原所需的最小份額數。</span><span class="sxs-lookup"><span data-stu-id="147fc-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="147fc-129">-確認</span><span class="sxs-lookup"><span data-stu-id="147fc-129">-Confirm</span></span>
<span data-ttu-id="147fc-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="147fc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="147fc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="147fc-131">-WhatIf</span></span>
<span data-ttu-id="147fc-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="147fc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="147fc-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="147fc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="147fc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="147fc-134">CommonParameters</span></span>
<span data-ttu-id="147fc-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="147fc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="147fc-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="147fc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="147fc-137">輸入</span><span class="sxs-lookup"><span data-stu-id="147fc-137">INPUTS</span></span>

### <span data-ttu-id="147fc-138">PSKeyVaultIdentityItem 中的 KeyVault。</span><span class="sxs-lookup"><span data-stu-id="147fc-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="147fc-139">輸出</span><span class="sxs-lookup"><span data-stu-id="147fc-139">OUTPUTS</span></span>

### <span data-ttu-id="147fc-140">System.object</span><span class="sxs-lookup"><span data-stu-id="147fc-140">System.Boolean</span></span>

## <span data-ttu-id="147fc-141">筆記</span><span class="sxs-lookup"><span data-stu-id="147fc-141">NOTES</span></span>

## <span data-ttu-id="147fc-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="147fc-142">RELATED LINKS</span></span>
