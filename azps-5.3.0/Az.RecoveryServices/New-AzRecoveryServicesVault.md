---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 3bb602d148b0843def129a1e4538d9ef8fdbe169
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98437283"
---
# <span data-ttu-id="b2d09-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b2d09-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="b2d09-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b2d09-102">SYNOPSIS</span></span>
<span data-ttu-id="b2d09-103">建立新的 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="b2d09-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="b2d09-104">句法</span><span class="sxs-lookup"><span data-stu-id="b2d09-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2d09-105">說明</span><span class="sxs-lookup"><span data-stu-id="b2d09-105">DESCRIPTION</span></span>
<span data-ttu-id="b2d09-106">**AzRecoveryServicesVault** Cmdlet 會建立新的 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="b2d09-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="b2d09-107">示例</span><span class="sxs-lookup"><span data-stu-id="b2d09-107">EXAMPLES</span></span>

### <span data-ttu-id="b2d09-108">範例1</span><span class="sxs-lookup"><span data-stu-id="b2d09-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="b2d09-109">在資源群組和指定的位置中建立恢復服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="b2d09-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="b2d09-110">參數</span><span class="sxs-lookup"><span data-stu-id="b2d09-110">PARAMETERS</span></span>

### <span data-ttu-id="b2d09-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2d09-111">-DefaultProfile</span></span>
<span data-ttu-id="b2d09-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b2d09-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2d09-113">-位置</span><span class="sxs-lookup"><span data-stu-id="b2d09-113">-Location</span></span>
<span data-ttu-id="b2d09-114">指定電子倉庫地理位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2d09-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="b2d09-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2d09-115">-Name</span></span>
<span data-ttu-id="b2d09-116">指定要建立的保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2d09-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="b2d09-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2d09-117">-ResourceGroupName</span></span>
<span data-ttu-id="b2d09-118">指定 Azure 資源群組的名稱，以在其中建立指定的復原服務物件，或從該資源群組中取得。</span><span class="sxs-lookup"><span data-stu-id="b2d09-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="b2d09-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="b2d09-119">-Tag</span></span>

<span data-ttu-id="b2d09-120">指定要新增到 [恢復服務] 保存庫的標籤</span><span class="sxs-lookup"><span data-stu-id="b2d09-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2d09-121">-確認</span><span class="sxs-lookup"><span data-stu-id="b2d09-121">-Confirm</span></span>
<span data-ttu-id="b2d09-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b2d09-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2d09-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2d09-123">-WhatIf</span></span>
<span data-ttu-id="b2d09-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2d09-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2d09-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2d09-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2d09-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2d09-126">CommonParameters</span></span>
<span data-ttu-id="b2d09-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b2d09-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2d09-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b2d09-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2d09-129">輸入</span><span class="sxs-lookup"><span data-stu-id="b2d09-129">INPUTS</span></span>

### <span data-ttu-id="b2d09-130">所有</span><span class="sxs-lookup"><span data-stu-id="b2d09-130">None</span></span>

## <span data-ttu-id="b2d09-131">輸出</span><span class="sxs-lookup"><span data-stu-id="b2d09-131">OUTPUTS</span></span>

### <span data-ttu-id="b2d09-132">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="b2d09-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b2d09-133">筆記</span><span class="sxs-lookup"><span data-stu-id="b2d09-133">NOTES</span></span>

## <span data-ttu-id="b2d09-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2d09-134">RELATED LINKS</span></span>

[<span data-ttu-id="b2d09-135">AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b2d09-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="b2d09-136">AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b2d09-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="b2d09-137">移除-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b2d09-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


