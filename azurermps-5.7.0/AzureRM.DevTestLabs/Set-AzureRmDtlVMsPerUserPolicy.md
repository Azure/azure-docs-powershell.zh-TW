---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 459ae0e3d18056c6579d4fd6248548155e1471cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448676"
---
# <span data-ttu-id="5d542-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="5d542-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="5d542-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5d542-102">SYNOPSIS</span></span>
<span data-ttu-id="5d542-103">在 DevTest Labs 中設定每位使用者的虛擬機器原則。</span><span class="sxs-lookup"><span data-stu-id="5d542-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d542-104">句法</span><span class="sxs-lookup"><span data-stu-id="5d542-104">SYNTAX</span></span>

### <span data-ttu-id="5d542-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="5d542-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d542-106">禁止</span><span class="sxs-lookup"><span data-stu-id="5d542-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d542-107">說明</span><span class="sxs-lookup"><span data-stu-id="5d542-107">DESCRIPTION</span></span>
<span data-ttu-id="5d542-108">**AzureRmDtlVMsPerUserPolicy** Cmdlet 會設定實驗室的每個使用者原則的虛擬機器原則，這會設定每位使用者允許的虛擬機器數量上限。</span><span class="sxs-lookup"><span data-stu-id="5d542-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="5d542-109">此 Cmdlet 會使用指定的資源群組和 lab 名稱來設定原則。</span><span class="sxs-lookup"><span data-stu-id="5d542-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="5d542-110">示例</span><span class="sxs-lookup"><span data-stu-id="5d542-110">EXAMPLES</span></span>

## <span data-ttu-id="5d542-111">參數</span><span class="sxs-lookup"><span data-stu-id="5d542-111">PARAMETERS</span></span>

### <span data-ttu-id="5d542-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d542-112">-DefaultProfile</span></span>
<span data-ttu-id="5d542-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5d542-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d542-114">-停用</span><span class="sxs-lookup"><span data-stu-id="5d542-114">-Disable</span></span>
<span data-ttu-id="5d542-115">表示此 Cmdlet 會停用實驗室的原則。</span><span class="sxs-lookup"><span data-stu-id="5d542-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="5d542-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="5d542-116">-Enable</span></span>
<span data-ttu-id="5d542-117">表示此 Cmdlet 可為 lab 啟用原則。</span><span class="sxs-lookup"><span data-stu-id="5d542-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="5d542-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="5d542-118">-LabName</span></span>
<span data-ttu-id="5d542-119">指定此 Cmdlet 針對每個使用者策略設定虛擬機器原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="5d542-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="5d542-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="5d542-120">-MaxVMs</span></span>
<span data-ttu-id="5d542-121">指定可在 lab 中建立的虛擬機器數目上限。</span><span class="sxs-lookup"><span data-stu-id="5d542-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d542-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d542-122">-ResourceGroupName</span></span>
<span data-ttu-id="5d542-123">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5d542-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="5d542-124">-確認</span><span class="sxs-lookup"><span data-stu-id="5d542-124">-Confirm</span></span>
<span data-ttu-id="5d542-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5d542-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d542-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d542-126">-WhatIf</span></span>
<span data-ttu-id="5d542-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5d542-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d542-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5d542-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d542-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d542-129">CommonParameters</span></span>
<span data-ttu-id="5d542-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5d542-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d542-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5d542-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d542-132">輸入</span><span class="sxs-lookup"><span data-stu-id="5d542-132">INPUTS</span></span>

### <span data-ttu-id="5d542-133">所有</span><span class="sxs-lookup"><span data-stu-id="5d542-133">None</span></span>
<span data-ttu-id="5d542-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="5d542-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5d542-135">輸出</span><span class="sxs-lookup"><span data-stu-id="5d542-135">OUTPUTS</span></span>

### <span data-ttu-id="5d542-136">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="5d542-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="5d542-137">這個 Cmdlet 會傳回指定可由 lab 中使用者建立的虛擬機器數上限的原則。</span><span class="sxs-lookup"><span data-stu-id="5d542-137">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="5d542-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5d542-138">NOTES</span></span>

## <span data-ttu-id="5d542-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="5d542-139">RELATED LINKS</span></span>

[<span data-ttu-id="5d542-140">AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="5d542-140">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


