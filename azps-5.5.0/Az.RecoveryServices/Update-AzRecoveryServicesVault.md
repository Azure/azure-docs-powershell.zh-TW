---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: cdde8169c4b068b986910dc3bfc5de446833f5ff
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100130926"
---
# <span data-ttu-id="f5760-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f5760-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="f5760-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5760-102">SYNOPSIS</span></span>
<span data-ttu-id="f5760-103">更新 MSI 至 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="f5760-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="f5760-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5760-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5760-105">說明</span><span class="sxs-lookup"><span data-stu-id="f5760-105">DESCRIPTION</span></span>
<span data-ttu-id="f5760-106">這個 Cmdlet 是用來從復原服務電子倉庫新增或移除 MSI。</span><span class="sxs-lookup"><span data-stu-id="f5760-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="f5760-107">使用-IdentityType param 將 SystemAssigned 身分識別指派至 RSVault。</span><span class="sxs-lookup"><span data-stu-id="f5760-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="f5760-108">使用 IdentityType None 從保存庫中移除 MSI。</span><span class="sxs-lookup"><span data-stu-id="f5760-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="f5760-109">示例</span><span class="sxs-lookup"><span data-stu-id="f5760-109">EXAMPLES</span></span>

### <span data-ttu-id="f5760-110">範例1</span><span class="sxs-lookup"><span data-stu-id="f5760-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="f5760-111">這個 Cmdlet 是用來將 SystemAssigned 身分識別新增到復原服務保存庫。</span><span class="sxs-lookup"><span data-stu-id="f5760-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="f5760-112">參數</span><span class="sxs-lookup"><span data-stu-id="f5760-112">PARAMETERS</span></span>

### <span data-ttu-id="f5760-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5760-113">-DefaultProfile</span></span>
<span data-ttu-id="f5760-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5760-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5760-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5760-115">-Name</span></span>

<span data-ttu-id="f5760-116">指定要更新的復原服務保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5760-116">Specifies the name of the recovery services vault to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5760-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5760-117">-ResourceGroupName</span></span>

<span data-ttu-id="f5760-118">指定 [恢復服務] 保存庫所在之 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5760-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5760-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="f5760-119">-IdentityType</span></span>
<span data-ttu-id="f5760-120">指派給復原服務保存庫的 MSI 類型。</span><span class="sxs-lookup"><span data-stu-id="f5760-120">The MSI type assigned to Recovery Services Vault.</span></span>

```yaml
Type: MSIdentity
Parameter Sets: (All)
Aliases:
Accepted values: SystemAssigned, None

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5760-121">-確認</span><span class="sxs-lookup"><span data-stu-id="f5760-121">-Confirm</span></span>
<span data-ttu-id="f5760-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5760-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5760-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5760-123">-WhatIf</span></span>
<span data-ttu-id="f5760-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5760-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5760-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5760-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5760-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5760-126">CommonParameters</span></span>
<span data-ttu-id="f5760-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5760-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5760-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f5760-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5760-129">輸入</span><span class="sxs-lookup"><span data-stu-id="f5760-129">INPUTS</span></span>

### <span data-ttu-id="f5760-130">System.object</span><span class="sxs-lookup"><span data-stu-id="f5760-130">System.String</span></span>

## <span data-ttu-id="f5760-131">輸出</span><span class="sxs-lookup"><span data-stu-id="f5760-131">OUTPUTS</span></span>

### <span data-ttu-id="f5760-132">[RecoveryServices]。電子倉庫</span><span class="sxs-lookup"><span data-stu-id="f5760-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="f5760-133">筆記</span><span class="sxs-lookup"><span data-stu-id="f5760-133">NOTES</span></span>

## <span data-ttu-id="f5760-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5760-134">RELATED LINKS</span></span>
