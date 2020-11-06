---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVM.md
ms.openlocfilehash: 3cc48d103867008b247ce480de43d1ccadc68d18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452528"
---
# <span data-ttu-id="993bb-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993bb-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="993bb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="993bb-102">SYNOPSIS</span></span>
<span data-ttu-id="993bb-103">從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="993bb-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="993bb-104">句法</span><span class="sxs-lookup"><span data-stu-id="993bb-104">SYNTAX</span></span>

### <span data-ttu-id="993bb-105">ResourceGroupNameParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="993bb-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="993bb-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="993bb-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="993bb-107">說明</span><span class="sxs-lookup"><span data-stu-id="993bb-107">DESCRIPTION</span></span>
<span data-ttu-id="993bb-108">**AzureRmVM** Cmdlet 會從 Azure 移除虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="993bb-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="993bb-109">示例</span><span class="sxs-lookup"><span data-stu-id="993bb-109">EXAMPLES</span></span>

### <span data-ttu-id="993bb-110">範例1：移除虛擬機器</span><span class="sxs-lookup"><span data-stu-id="993bb-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="993bb-111">這個命令會從 [資源群組 ResourceGroup11] 中移除名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="993bb-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="993bb-112">參數</span><span class="sxs-lookup"><span data-stu-id="993bb-112">PARAMETERS</span></span>

### <span data-ttu-id="993bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="993bb-113">-DefaultProfile</span></span>
<span data-ttu-id="993bb-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="993bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="993bb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="993bb-115">-Force</span></span>
<span data-ttu-id="993bb-116">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="993bb-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="993bb-117">-識別碼</span><span class="sxs-lookup"><span data-stu-id="993bb-117">-Id</span></span>
<span data-ttu-id="993bb-118">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="993bb-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="993bb-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="993bb-119">-Name</span></span>
<span data-ttu-id="993bb-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="993bb-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="993bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="993bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="993bb-122">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="993bb-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="993bb-123">-確認</span><span class="sxs-lookup"><span data-stu-id="993bb-123">-Confirm</span></span>
<span data-ttu-id="993bb-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="993bb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="993bb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="993bb-125">-WhatIf</span></span>
<span data-ttu-id="993bb-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="993bb-126">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="993bb-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="993bb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="993bb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="993bb-128">CommonParameters</span></span>
<span data-ttu-id="993bb-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="993bb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="993bb-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="993bb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="993bb-131">輸入</span><span class="sxs-lookup"><span data-stu-id="993bb-131">INPUTS</span></span>

## <span data-ttu-id="993bb-132">輸出</span><span class="sxs-lookup"><span data-stu-id="993bb-132">OUTPUTS</span></span>

## <span data-ttu-id="993bb-133">筆記</span><span class="sxs-lookup"><span data-stu-id="993bb-133">NOTES</span></span>

## <span data-ttu-id="993bb-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="993bb-134">RELATED LINKS</span></span>

[<span data-ttu-id="993bb-135">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993bb-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="993bb-136">新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993bb-136">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="993bb-137">重新開機-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993bb-137">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="993bb-138">開始-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993bb-138">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="993bb-139">停止 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993bb-139">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="993bb-140">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="993bb-140">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


