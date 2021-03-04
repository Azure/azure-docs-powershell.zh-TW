---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesVault.md
ms.openlocfilehash: 104bb05b4a01f5407c56e6c89de632a1ec5ab475
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906422"
---
# <span data-ttu-id="be85e-101">Update-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="be85e-101">Update-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="be85e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="be85e-102">SYNOPSIS</span></span>
<span data-ttu-id="be85e-103">將 MSI 更新至復原服務儲存庫。</span><span class="sxs-lookup"><span data-stu-id="be85e-103">Updates MSI to the recovery services vault.</span></span>

## <span data-ttu-id="be85e-104">語法</span><span class="sxs-lookup"><span data-stu-id="be85e-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesVault -ResourceGroupName <string> -Name <string> -IdentityType <MSIdentity>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be85e-105">描述</span><span class="sxs-lookup"><span data-stu-id="be85e-105">DESCRIPTION</span></span>
<span data-ttu-id="be85e-106">此 Cmdlet 用來從復原服務儲存庫新增或移除 MSI。</span><span class="sxs-lookup"><span data-stu-id="be85e-106">This cmdlet is used to add or remove  the MSI from the recovery services vault.</span></span> <span data-ttu-id="be85e-107">使用 -IdentityType param 將 SystemAssigned 身分識別指派給 RSVault。</span><span class="sxs-lookup"><span data-stu-id="be85e-107">Use -IdentityType param to assign a SystemAssigned identity to the RSVault.</span></span> <span data-ttu-id="be85e-108">使用 IdentityType None 從儲存庫移除 MSI。</span><span class="sxs-lookup"><span data-stu-id="be85e-108">Use IdentityType None to remove the MSI from the vault.</span></span>

## <span data-ttu-id="be85e-109">例子</span><span class="sxs-lookup"><span data-stu-id="be85e-109">EXAMPLES</span></span>

### <span data-ttu-id="be85e-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="be85e-110">Example 1</span></span>
```powershell
PS C:\> Update-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName" -IdentityType SystemAssigned
```

<span data-ttu-id="be85e-111">此 Cmdlet 用來將 SystemAssigned 身分識別新加到復原服務儲存庫。</span><span class="sxs-lookup"><span data-stu-id="be85e-111">This cmdlet is used to add a SystemAssigned identity to a recovery services vault.</span></span>

## <span data-ttu-id="be85e-112">參數</span><span class="sxs-lookup"><span data-stu-id="be85e-112">PARAMETERS</span></span>

### <span data-ttu-id="be85e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be85e-113">-DefaultProfile</span></span>
<span data-ttu-id="be85e-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="be85e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be85e-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="be85e-115">-Name</span></span>

<span data-ttu-id="be85e-116">指定要更新的復原服務庫名稱。</span><span class="sxs-lookup"><span data-stu-id="be85e-116">Specifies the name of the recovery services vault to update.</span></span>

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

### <span data-ttu-id="be85e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be85e-117">-ResourceGroupName</span></span>

<span data-ttu-id="be85e-118">指定有復原服務儲存庫的 Azure 資源組名。</span><span class="sxs-lookup"><span data-stu-id="be85e-118">Specifies the name of the Azure resource group where recovery services vault is present.</span></span>

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

### <span data-ttu-id="be85e-119">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="be85e-119">-IdentityType</span></span>
<span data-ttu-id="be85e-120">指派給復原服務儲存庫的 MSI 類型。</span><span class="sxs-lookup"><span data-stu-id="be85e-120">The MSI type assigned to Recovery Services Vault.</span></span>

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

### <span data-ttu-id="be85e-121">-確認</span><span class="sxs-lookup"><span data-stu-id="be85e-121">-Confirm</span></span>
<span data-ttu-id="be85e-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="be85e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be85e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be85e-123">-WhatIf</span></span>
<span data-ttu-id="be85e-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="be85e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be85e-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="be85e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be85e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be85e-126">CommonParameters</span></span>
<span data-ttu-id="be85e-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="be85e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be85e-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="be85e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be85e-129">輸入</span><span class="sxs-lookup"><span data-stu-id="be85e-129">INPUTS</span></span>

### <span data-ttu-id="be85e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="be85e-130">System.String</span></span>

## <span data-ttu-id="be85e-131">輸出</span><span class="sxs-lookup"><span data-stu-id="be85e-131">OUTPUTS</span></span>

### <span data-ttu-id="be85e-132">Microsoft.Azure.management.RecoveryServices.models.Vault</span><span class="sxs-lookup"><span data-stu-id="be85e-132">Microsoft.Azure.Management.RecoveryServices.Models.Vault</span></span>

## <span data-ttu-id="be85e-133">筆記</span><span class="sxs-lookup"><span data-stu-id="be85e-133">NOTES</span></span>

## <span data-ttu-id="be85e-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="be85e-134">RELATED LINKS</span></span>
