---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 95908e6b0976baf2ce9f3c117f54a6f1552e4957
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625182"
---
# <span data-ttu-id="b9334-101">Set-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="b9334-101">Set-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="b9334-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9334-102">SYNOPSIS</span></span>
<span data-ttu-id="b9334-103">在 DevTest Labs 中設定實驗室的每個實驗室原則的虛擬機器原則。</span><span class="sxs-lookup"><span data-stu-id="b9334-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9334-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9334-104">SYNTAX</span></span>

### <span data-ttu-id="b9334-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="b9334-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9334-106">禁止</span><span class="sxs-lookup"><span data-stu-id="b9334-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9334-107">說明</span><span class="sxs-lookup"><span data-stu-id="b9334-107">DESCRIPTION</span></span>
<span data-ttu-id="b9334-108">**AzureRmDtlVMsPerLabPolicy** Cmdlet 會設定實驗室的每個實驗室原則的虛擬機器原則，這會設定實驗室所允許的虛擬機器總數目。</span><span class="sxs-lookup"><span data-stu-id="b9334-108">The **Set-AzureRmDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="b9334-109">此 Cmdlet 會使用指定的資源群組和 lab 名稱來設定原則。</span><span class="sxs-lookup"><span data-stu-id="b9334-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="b9334-110">示例</span><span class="sxs-lookup"><span data-stu-id="b9334-110">EXAMPLES</span></span>

## <span data-ttu-id="b9334-111">參數</span><span class="sxs-lookup"><span data-stu-id="b9334-111">PARAMETERS</span></span>

### <span data-ttu-id="b9334-112">-停用</span><span class="sxs-lookup"><span data-stu-id="b9334-112">-Disable</span></span>
<span data-ttu-id="b9334-113">表示此 Cmdlet 會停用實驗室的原則。</span><span class="sxs-lookup"><span data-stu-id="b9334-113">Indicates that this cmdlet disables the policy of the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9334-114">-啟用</span><span class="sxs-lookup"><span data-stu-id="b9334-114">-Enable</span></span>
<span data-ttu-id="b9334-115">表示此 Cmdlet 啟用 lab 原則。</span><span class="sxs-lookup"><span data-stu-id="b9334-115">Indicates that this cmdlet enables the policy of the lab.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9334-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="b9334-116">-LabName</span></span>
<span data-ttu-id="b9334-117">指定此 Cmdlet 針對每個實驗室原則設定虛擬機器的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="b9334-117">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9334-118">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="b9334-118">-MaxVMs</span></span>
<span data-ttu-id="b9334-119">指定可在 lab 中建立的虛擬機器數目上限。</span><span class="sxs-lookup"><span data-stu-id="b9334-119">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9334-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9334-120">-ResourceGroupName</span></span>
<span data-ttu-id="b9334-121">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9334-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9334-122">-確認</span><span class="sxs-lookup"><span data-stu-id="b9334-122">-Confirm</span></span>
<span data-ttu-id="b9334-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b9334-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9334-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9334-124">-WhatIf</span></span>
<span data-ttu-id="b9334-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b9334-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9334-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9334-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9334-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9334-127">-DefaultProfile</span></span>
<span data-ttu-id="b9334-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9334-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9334-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9334-129">CommonParameters</span></span>
<span data-ttu-id="b9334-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9334-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9334-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b9334-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9334-132">輸入</span><span class="sxs-lookup"><span data-stu-id="b9334-132">INPUTS</span></span>

## <span data-ttu-id="b9334-133">輸出</span><span class="sxs-lookup"><span data-stu-id="b9334-133">OUTPUTS</span></span>

### <span data-ttu-id="b9334-134">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="b9334-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="b9334-135">這個 Cmdlet 會傳回指定可在 lab 中建立的虛擬機器數上限的原則。</span><span class="sxs-lookup"><span data-stu-id="b9334-135">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created in the lab.</span></span>

## <span data-ttu-id="b9334-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b9334-136">NOTES</span></span>

## <span data-ttu-id="b9334-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9334-137">RELATED LINKS</span></span>

[<span data-ttu-id="b9334-138">AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="b9334-138">Get-AzureRmDtlVMsPerLabPolicy</span></span>](./Get-AzureRmDtlVMsPerLabPolicy.md)


