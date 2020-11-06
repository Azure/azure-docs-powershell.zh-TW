---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 70AA9747-232E-40F2-845C-35A779F51CD2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssVM.md
ms.openlocfilehash: e4c3199218294e1a75a2bc62dd148c3409159ed7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446877"
---
# <span data-ttu-id="1192d-101">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="1192d-101">Set-AzureRmVmssVM</span></span>

## <span data-ttu-id="1192d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1192d-102">SYNOPSIS</span></span>
<span data-ttu-id="1192d-103">修改 VMSS 實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="1192d-103">Modifies the state of a VMSS instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1192d-104">句法</span><span class="sxs-lookup"><span data-stu-id="1192d-104">SYNTAX</span></span>

### <span data-ttu-id="1192d-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="1192d-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1192d-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="1192d-106">FriendMethod</span></span>
```
Set-AzureRmVmssVM [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String> [-ReimageAll]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1192d-107">說明</span><span class="sxs-lookup"><span data-stu-id="1192d-107">DESCRIPTION</span></span>
<span data-ttu-id="1192d-108">**AzureRmVmssVM** Cmdlet 會修改虛擬機器縮放集 (VMSS) 實例的狀態。</span><span class="sxs-lookup"><span data-stu-id="1192d-108">The **Set-AzureRmVmssVM** cmdlet modifies the state of a Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="1192d-109">示例</span><span class="sxs-lookup"><span data-stu-id="1192d-109">EXAMPLES</span></span>

## <span data-ttu-id="1192d-110">參數</span><span class="sxs-lookup"><span data-stu-id="1192d-110">PARAMETERS</span></span>

### <span data-ttu-id="1192d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1192d-111">-DefaultProfile</span></span>
<span data-ttu-id="1192d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1192d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1192d-113">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1192d-113">-InstanceId</span></span>
<span data-ttu-id="1192d-114">指定此 Cmdlet 修改狀態的 VMSS 實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="1192d-114">Specifies the ID of the VMSS instance for which this cmdlet modifies state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1192d-115">-重新映射</span><span class="sxs-lookup"><span data-stu-id="1192d-115">-Reimage</span></span>
<span data-ttu-id="1192d-116">表示此 Cmdlet reimages VMSS 實例。</span><span class="sxs-lookup"><span data-stu-id="1192d-116">Indicates that this cmdlet reimages the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1192d-117">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="1192d-117">-ReimageAll</span></span>
<span data-ttu-id="1192d-118">表示 Cmdlet reimages VMSS 實例中的所有磁片。</span><span class="sxs-lookup"><span data-stu-id="1192d-118">Indicates that the cmdlet reimages all the disks in the VMSS instance.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1192d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1192d-119">-ResourceGroupName</span></span>
<span data-ttu-id="1192d-120">指定包含 VMSS 實例之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1192d-120">Specifies the name of the resource group that contains the VMSS instance.</span></span>

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

### <span data-ttu-id="1192d-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="1192d-121">-VMScaleSetName</span></span>
<span data-ttu-id="1192d-122">指定此 Cmdlet 所修改之 VMSS 實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="1192d-122">Specifies the name of the VMSS instance that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1192d-123">-確認</span><span class="sxs-lookup"><span data-stu-id="1192d-123">-Confirm</span></span>
<span data-ttu-id="1192d-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1192d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1192d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1192d-125">-WhatIf</span></span>
<span data-ttu-id="1192d-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1192d-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1192d-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1192d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1192d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1192d-128">CommonParameters</span></span>
<span data-ttu-id="1192d-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1192d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1192d-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1192d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1192d-131">輸入</span><span class="sxs-lookup"><span data-stu-id="1192d-131">INPUTS</span></span>

## <span data-ttu-id="1192d-132">輸出</span><span class="sxs-lookup"><span data-stu-id="1192d-132">OUTPUTS</span></span>

## <span data-ttu-id="1192d-133">筆記</span><span class="sxs-lookup"><span data-stu-id="1192d-133">NOTES</span></span>

## <span data-ttu-id="1192d-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="1192d-134">RELATED LINKS</span></span>

[<span data-ttu-id="1192d-135">AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="1192d-135">Get-AzureRmVmssVM</span></span>](./Get-AzureRmVmssVM.md)
