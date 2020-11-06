---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 08166ea1ebe4c78521a68f9e5423a7947e78b699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455084"
---
# <span data-ttu-id="7fb65-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7fb65-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="7fb65-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7fb65-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb65-103">建立新的 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="7fb65-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fb65-104">句法</span><span class="sxs-lookup"><span data-stu-id="7fb65-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fb65-105">說明</span><span class="sxs-lookup"><span data-stu-id="7fb65-105">DESCRIPTION</span></span>
<span data-ttu-id="7fb65-106">**AzureRmRecoveryServicesVault** Cmdlet 會建立新的 [恢復服務] 保存庫。</span><span class="sxs-lookup"><span data-stu-id="7fb65-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="7fb65-107">示例</span><span class="sxs-lookup"><span data-stu-id="7fb65-107">EXAMPLES</span></span>

### <span data-ttu-id="7fb65-108">範例1</span><span class="sxs-lookup"><span data-stu-id="7fb65-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="7fb65-109">在資源群組和指定的位置中建立恢復服務電子倉庫。</span><span class="sxs-lookup"><span data-stu-id="7fb65-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="7fb65-110">參數</span><span class="sxs-lookup"><span data-stu-id="7fb65-110">PARAMETERS</span></span>

### <span data-ttu-id="7fb65-111">-位置</span><span class="sxs-lookup"><span data-stu-id="7fb65-111">-Location</span></span>
<span data-ttu-id="7fb65-112">指定電子倉庫地理位置的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fb65-112">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb65-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="7fb65-113">-Name</span></span>
<span data-ttu-id="7fb65-114">指定要建立的保存庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7fb65-114">Specifies the name of the vault to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb65-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb65-115">-ResourceGroupName</span></span>
<span data-ttu-id="7fb65-116">指定 Azure 資源群組的名稱，以在其中建立指定的復原服務物件，或從該資源群組中取得。</span><span class="sxs-lookup"><span data-stu-id="7fb65-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb65-117">-確認</span><span class="sxs-lookup"><span data-stu-id="7fb65-117">-Confirm</span></span>
<span data-ttu-id="7fb65-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7fb65-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fb65-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fb65-119">-WhatIf</span></span>
<span data-ttu-id="7fb65-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7fb65-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7fb65-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7fb65-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fb65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb65-122">-DefaultProfile</span></span>
<span data-ttu-id="7fb65-123">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7fb65-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fb65-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb65-124">CommonParameters</span></span>
<span data-ttu-id="7fb65-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7fb65-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb65-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7fb65-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb65-127">輸入</span><span class="sxs-lookup"><span data-stu-id="7fb65-127">INPUTS</span></span>

### <span data-ttu-id="7fb65-128">所有</span><span class="sxs-lookup"><span data-stu-id="7fb65-128">None</span></span>

## <span data-ttu-id="7fb65-129">輸出</span><span class="sxs-lookup"><span data-stu-id="7fb65-129">OUTPUTS</span></span>

### <span data-ttu-id="7fb65-130">ARSVault 中的 RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7fb65-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7fb65-131">筆記</span><span class="sxs-lookup"><span data-stu-id="7fb65-131">NOTES</span></span>

## <span data-ttu-id="7fb65-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="7fb65-132">RELATED LINKS</span></span>

[<span data-ttu-id="7fb65-133">AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7fb65-133">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="7fb65-134">AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7fb65-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="7fb65-135">移除-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7fb65-135">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


