---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968829"
---
# <span data-ttu-id="facc3-101">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="facc3-101">Set-WAPackVMRole</span></span>

## <span data-ttu-id="facc3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="facc3-102">SYNOPSIS</span></span>
<span data-ttu-id="facc3-103">變更虛擬機器角色的 [實例計數] 屬性。</span><span class="sxs-lookup"><span data-stu-id="facc3-103">Changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="facc3-104">句法</span><span class="sxs-lookup"><span data-stu-id="facc3-104">SYNTAX</span></span>

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="facc3-105">說明</span><span class="sxs-lookup"><span data-stu-id="facc3-105">DESCRIPTION</span></span>
<span data-ttu-id="facc3-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="facc3-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="facc3-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="facc3-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="facc3-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="facc3-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="facc3-109">**WAPackVMRole** Cmdlet 會變更虛擬機器角色的 [實例計數] 屬性。</span><span class="sxs-lookup"><span data-stu-id="facc3-109">The **Set-WAPackVMRole** cmdlet changes the instance count property of a virtual machine role.</span></span>

## <span data-ttu-id="facc3-110">示例</span><span class="sxs-lookup"><span data-stu-id="facc3-110">EXAMPLES</span></span>

### <span data-ttu-id="facc3-111">範例1：指定虛擬機器角色的實例計數</span><span class="sxs-lookup"><span data-stu-id="facc3-111">Example 1: Specify the instance count for a virtual machine role</span></span>
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

<span data-ttu-id="facc3-112">第一個命令會使用 **WAPackVMRole** Cmdlet 取得名為 ContosoVMRole01 的虛擬機器角色，然後將該物件儲存在 $VMRole 變數中。</span><span class="sxs-lookup"><span data-stu-id="facc3-112">The first command gets the virtual machine role named ContosoVMRole01 by using the **Get-WAPackVMRole** cmdlet, and then stores that object in the $VMRole variable.</span></span>

<span data-ttu-id="facc3-113">第二個和最後一個命令會將儲存在 $VMRole 的虛擬機器角色的新實例計數設定為3。</span><span class="sxs-lookup"><span data-stu-id="facc3-113">The second and final command sets the new instance count of the virtual machine role stored in $VMRole to 3.</span></span>

## <span data-ttu-id="facc3-114">參數</span><span class="sxs-lookup"><span data-stu-id="facc3-114">PARAMETERS</span></span>

### <span data-ttu-id="facc3-115">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="facc3-115">-InstanceCount</span></span>
<span data-ttu-id="facc3-116">指定虛擬機器角色的實例計數。</span><span class="sxs-lookup"><span data-stu-id="facc3-116">Specifies the instance count for a virtual machine role.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facc3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="facc3-117">-PassThru</span></span>
<span data-ttu-id="facc3-118">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="facc3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="facc3-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="facc3-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facc3-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="facc3-120">-Profile</span></span>
<span data-ttu-id="facc3-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="facc3-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="facc3-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="facc3-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="facc3-123">-VMRole</span><span class="sxs-lookup"><span data-stu-id="facc3-123">-VMRole</span></span>
<span data-ttu-id="facc3-124">指定虛擬機器角色。</span><span class="sxs-lookup"><span data-stu-id="facc3-124">Specifies a virtual machine role.</span></span>
<span data-ttu-id="facc3-125">若要取得虛擬機器角色，請使用 **WAPackVMRole** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="facc3-125">To obtain a virtual machine role, use the **Get-WAPackVMRole** cmdlet.</span></span>

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="facc3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="facc3-126">CommonParameters</span></span>
<span data-ttu-id="facc3-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="facc3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="facc3-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="facc3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="facc3-129">輸入</span><span class="sxs-lookup"><span data-stu-id="facc3-129">INPUTS</span></span>

## <span data-ttu-id="facc3-130">輸出</span><span class="sxs-lookup"><span data-stu-id="facc3-130">OUTPUTS</span></span>

## <span data-ttu-id="facc3-131">筆記</span><span class="sxs-lookup"><span data-stu-id="facc3-131">NOTES</span></span>

## <span data-ttu-id="facc3-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="facc3-132">RELATED LINKS</span></span>

[<span data-ttu-id="facc3-133">WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="facc3-133">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="facc3-134">新-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="facc3-134">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="facc3-135">移除-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="facc3-135">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)


