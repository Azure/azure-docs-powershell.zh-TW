---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: b3790105f2404cc7bf50ef1200ce0978e8f0b15d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453524"
---
# <span data-ttu-id="26927-101">Set-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="26927-101">Set-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="26927-102">摘要</span><span class="sxs-lookup"><span data-stu-id="26927-102">SYNOPSIS</span></span>
<span data-ttu-id="26927-103">在 DevTest Labs 中設定每位使用者的虛擬機器原則。</span><span class="sxs-lookup"><span data-stu-id="26927-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26927-104">句法</span><span class="sxs-lookup"><span data-stu-id="26927-104">SYNTAX</span></span>

### <span data-ttu-id="26927-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="26927-105">Enable (Default)</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26927-106">禁止</span><span class="sxs-lookup"><span data-stu-id="26927-106">Disable</span></span>
```
Set-AzureRmDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26927-107">說明</span><span class="sxs-lookup"><span data-stu-id="26927-107">DESCRIPTION</span></span>
<span data-ttu-id="26927-108">**AzureRmDtlVMsPerUserPolicy** Cmdlet 會設定實驗室的每個使用者原則的虛擬機器原則，這會設定每位使用者允許的虛擬機器數量上限。</span><span class="sxs-lookup"><span data-stu-id="26927-108">The **Set-AzureRmDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="26927-109">此 Cmdlet 會使用指定的資源群組和 lab 名稱來設定原則。</span><span class="sxs-lookup"><span data-stu-id="26927-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="26927-110">示例</span><span class="sxs-lookup"><span data-stu-id="26927-110">EXAMPLES</span></span>

## <span data-ttu-id="26927-111">參數</span><span class="sxs-lookup"><span data-stu-id="26927-111">PARAMETERS</span></span>

### <span data-ttu-id="26927-112">-停用</span><span class="sxs-lookup"><span data-stu-id="26927-112">-Disable</span></span>
<span data-ttu-id="26927-113">表示此 Cmdlet 會停用實驗室的原則。</span><span class="sxs-lookup"><span data-stu-id="26927-113">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="26927-114">-啟用</span><span class="sxs-lookup"><span data-stu-id="26927-114">-Enable</span></span>
<span data-ttu-id="26927-115">表示此 Cmdlet 可為 lab 啟用原則。</span><span class="sxs-lookup"><span data-stu-id="26927-115">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="26927-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="26927-116">-LabName</span></span>
<span data-ttu-id="26927-117">指定此 Cmdlet 針對每個使用者策略設定虛擬機器原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="26927-117">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="26927-118">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="26927-118">-MaxVMs</span></span>
<span data-ttu-id="26927-119">指定可在 lab 中建立的虛擬機器數目上限。</span><span class="sxs-lookup"><span data-stu-id="26927-119">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="26927-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26927-120">-ResourceGroupName</span></span>
<span data-ttu-id="26927-121">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="26927-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="26927-122">-確認</span><span class="sxs-lookup"><span data-stu-id="26927-122">-Confirm</span></span>
<span data-ttu-id="26927-123">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="26927-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26927-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26927-124">-WhatIf</span></span>
<span data-ttu-id="26927-125">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="26927-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26927-126">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="26927-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26927-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26927-127">-DefaultProfile</span></span>
<span data-ttu-id="26927-128">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="26927-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26927-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26927-129">CommonParameters</span></span>
<span data-ttu-id="26927-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="26927-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26927-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="26927-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26927-132">輸入</span><span class="sxs-lookup"><span data-stu-id="26927-132">INPUTS</span></span>

## <span data-ttu-id="26927-133">輸出</span><span class="sxs-lookup"><span data-stu-id="26927-133">OUTPUTS</span></span>

### <span data-ttu-id="26927-134">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="26927-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="26927-135">這個 Cmdlet 會傳回指定可由 lab 中使用者建立的虛擬機器數上限的原則。</span><span class="sxs-lookup"><span data-stu-id="26927-135">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="26927-136">筆記</span><span class="sxs-lookup"><span data-stu-id="26927-136">NOTES</span></span>

## <span data-ttu-id="26927-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="26927-137">RELATED LINKS</span></span>

[<span data-ttu-id="26927-138">AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="26927-138">Get-AzureRmDtlVMsPerUserPolicy</span></span>](./Get-AzureRmDtlVMsPerUserPolicy.md)


