---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: e1c5fad70147300bb08fdafb94fb81079a02ea00
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447808"
---
# <span data-ttu-id="26d22-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="26d22-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="26d22-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26d22-102">SYNOPSIS</span></span>
<span data-ttu-id="26d22-103">在 DevTest Labs 中設定實驗的 [允許的虛擬機器大小] 原則。</span><span class="sxs-lookup"><span data-stu-id="26d22-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26d22-104">句法</span><span class="sxs-lookup"><span data-stu-id="26d22-104">SYNTAX</span></span>

### <span data-ttu-id="26d22-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="26d22-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26d22-106">禁止</span><span class="sxs-lookup"><span data-stu-id="26d22-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26d22-107">說明</span><span class="sxs-lookup"><span data-stu-id="26d22-107">DESCRIPTION</span></span>
<span data-ttu-id="26d22-108">**AzureRmDtlAllowedVMSizesPolicy** Cmdlet 會設定允許的虛擬機器大小原則，此原則會指定實驗中允許的虛擬機器大小清單。</span><span class="sxs-lookup"><span data-stu-id="26d22-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="26d22-109">此 Cmdlet 會使用指定的資源群組和 lab 名稱來設定原則。</span><span class="sxs-lookup"><span data-stu-id="26d22-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="26d22-110">示例</span><span class="sxs-lookup"><span data-stu-id="26d22-110">EXAMPLES</span></span>

## <span data-ttu-id="26d22-111">參數</span><span class="sxs-lookup"><span data-stu-id="26d22-111">PARAMETERS</span></span>

### <span data-ttu-id="26d22-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26d22-112">-DefaultProfile</span></span>
<span data-ttu-id="26d22-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="26d22-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26d22-114">-停用</span><span class="sxs-lookup"><span data-stu-id="26d22-114">-Disable</span></span>
<span data-ttu-id="26d22-115">表示此 Cmdlet 會停用原則。</span><span class="sxs-lookup"><span data-stu-id="26d22-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d22-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="26d22-116">-Enable</span></span>
<span data-ttu-id="26d22-117">表示此 Cmdlet 啟用原則。</span><span class="sxs-lookup"><span data-stu-id="26d22-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d22-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="26d22-118">-LabName</span></span>
<span data-ttu-id="26d22-119">指定此 Cmdlet 設定虛擬機器大小原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="26d22-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="26d22-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26d22-120">-ResourceGroupName</span></span>
<span data-ttu-id="26d22-121">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26d22-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26d22-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="26d22-122">-VmSizes</span></span>
<span data-ttu-id="26d22-123">指定為字串陣列，即在 lab 中允許的虛擬機器大小清單。</span><span class="sxs-lookup"><span data-stu-id="26d22-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26d22-124">-確認</span><span class="sxs-lookup"><span data-stu-id="26d22-124">-Confirm</span></span>
<span data-ttu-id="26d22-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26d22-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26d22-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26d22-126">-WhatIf</span></span>
<span data-ttu-id="26d22-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26d22-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26d22-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26d22-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26d22-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26d22-129">CommonParameters</span></span>
<span data-ttu-id="26d22-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26d22-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26d22-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26d22-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26d22-132">輸入</span><span class="sxs-lookup"><span data-stu-id="26d22-132">INPUTS</span></span>

### <span data-ttu-id="26d22-133">所有</span><span class="sxs-lookup"><span data-stu-id="26d22-133">None</span></span>
<span data-ttu-id="26d22-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="26d22-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26d22-135">輸出</span><span class="sxs-lookup"><span data-stu-id="26d22-135">OUTPUTS</span></span>

### <span data-ttu-id="26d22-136">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="26d22-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="26d22-137">這個 Cmdlet 會傳回指定實驗室所允許的虛擬機器大小清單的原則。</span><span class="sxs-lookup"><span data-stu-id="26d22-137">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="26d22-138">筆記</span><span class="sxs-lookup"><span data-stu-id="26d22-138">NOTES</span></span>

## <span data-ttu-id="26d22-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="26d22-139">RELATED LINKS</span></span>

[<span data-ttu-id="26d22-140">AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="26d22-140">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)

