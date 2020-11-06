---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: fa8681a8dab5aaba6d82b03a8b3885fd453e1faa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452532"
---
# <span data-ttu-id="b02ea-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b02ea-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="b02ea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b02ea-102">SYNOPSIS</span></span>
<span data-ttu-id="b02ea-103">取得 VMSS 的屬性。</span><span class="sxs-lookup"><span data-stu-id="b02ea-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b02ea-104">句法</span><span class="sxs-lookup"><span data-stu-id="b02ea-104">SYNTAX</span></span>

### <span data-ttu-id="b02ea-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="b02ea-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b02ea-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="b02ea-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b02ea-107">說明</span><span class="sxs-lookup"><span data-stu-id="b02ea-107">DESCRIPTION</span></span>
<span data-ttu-id="b02ea-108">**AzureRmVmss** Cmdlet 會取得虛擬機器縮放集 (VMSS) 的模型和實例視圖。</span><span class="sxs-lookup"><span data-stu-id="b02ea-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b02ea-109">模型視圖是使用者指定的虛擬機器屬性。</span><span class="sxs-lookup"><span data-stu-id="b02ea-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="b02ea-110">[實例] 視圖是虛擬機器的實例層級狀態。</span><span class="sxs-lookup"><span data-stu-id="b02ea-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="b02ea-111">指定 *Status* 參數，只取得虛擬機器的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="b02ea-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="b02ea-112">示例</span><span class="sxs-lookup"><span data-stu-id="b02ea-112">EXAMPLES</span></span>

### <span data-ttu-id="b02ea-113">範例1：取得 VMSS 的屬性</span><span class="sxs-lookup"><span data-stu-id="b02ea-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="b02ea-114">這個命令會取得屬於名為 Group001 之資源群組之名為 VMSS001 的 VMSS 屬性。</span><span class="sxs-lookup"><span data-stu-id="b02ea-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="b02ea-115">由於命令不會指定 *InstanceView* 切換參數，因此 Cmdlet 會取得虛擬機器的模型視圖。</span><span class="sxs-lookup"><span data-stu-id="b02ea-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="b02ea-116">參數</span><span class="sxs-lookup"><span data-stu-id="b02ea-116">PARAMETERS</span></span>

### <span data-ttu-id="b02ea-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b02ea-117">-DefaultProfile</span></span>
<span data-ttu-id="b02ea-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b02ea-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b02ea-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="b02ea-119">-InstanceView</span></span>
<span data-ttu-id="b02ea-120">表示此 Cmdlet 只會取得虛擬機器的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="b02ea-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="b02ea-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b02ea-121">-ResourceGroupName</span></span>
<span data-ttu-id="b02ea-122">指定 VMSS 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b02ea-122">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b02ea-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b02ea-123">-VMScaleSetName</span></span>
<span data-ttu-id="b02ea-124">Species VMSS 的名稱。</span><span class="sxs-lookup"><span data-stu-id="b02ea-124">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b02ea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b02ea-125">CommonParameters</span></span>
<span data-ttu-id="b02ea-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b02ea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b02ea-127">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b02ea-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b02ea-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b02ea-128">INPUTS</span></span>

## <span data-ttu-id="b02ea-129">輸出</span><span class="sxs-lookup"><span data-stu-id="b02ea-129">OUTPUTS</span></span>

### <span data-ttu-id="b02ea-130">這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="b02ea-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="b02ea-131">筆記</span><span class="sxs-lookup"><span data-stu-id="b02ea-131">NOTES</span></span>

## <span data-ttu-id="b02ea-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="b02ea-132">RELATED LINKS</span></span>

[<span data-ttu-id="b02ea-133">新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b02ea-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="b02ea-134">移除-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b02ea-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="b02ea-135">重新開機-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b02ea-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="b02ea-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b02ea-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="b02ea-137">開始-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b02ea-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="b02ea-138">停止 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b02ea-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="b02ea-139">更新-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b02ea-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


