---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968836"
---
# <span data-ttu-id="7d5ae-101">New-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7d5ae-101">New-WAPackVMRole</span></span>

## <span data-ttu-id="7d5ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d5ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7d5ae-103">建立虛擬機器角色。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-103">Creates a virtual machine role.</span></span>

## <span data-ttu-id="7d5ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d5ae-104">SYNTAX</span></span>

### <span data-ttu-id="7d5ae-105">QuickCreate (預設) </span><span class="sxs-lookup"><span data-stu-id="7d5ae-105">QuickCreate (Default)</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7d5ae-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="7d5ae-106">FromCloudService</span></span>
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7d5ae-107">說明</span><span class="sxs-lookup"><span data-stu-id="7d5ae-107">DESCRIPTION</span></span>
<span data-ttu-id="7d5ae-108">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7d5ae-109">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7d5ae-110">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7d5ae-111">**新的-WAPackVMRole** Cmdlet 會建立虛擬機器角色。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-111">The **New-WAPackVMRole** cmdlet creates a virtual machine role.</span></span>

## <span data-ttu-id="7d5ae-112">示例</span><span class="sxs-lookup"><span data-stu-id="7d5ae-112">EXAMPLES</span></span>

### <span data-ttu-id="7d5ae-113">範例1：建立虛擬電腦角色 (模擬 WAP 行為) </span><span class="sxs-lookup"><span data-stu-id="7d5ae-113">Example 1: Create a virtual machine role (emulating WAP behavior)</span></span>
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

<span data-ttu-id="7d5ae-114">因為我們不會指定任何雲端服務 (模擬 WAP 行為) ，所以命令會建立一個雲端服務，讓我們將其名稱與虛擬電腦角色相同。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-114">Since we do not specify any cloud service (emulating WAP behavior), the command will create a cloud service for us which will have the same name as the virtual machine role.</span></span>
<span data-ttu-id="7d5ae-115">在這種情況下，下列命令會建立名稱為 ContosoVMRole01、label ContosoVMRoleLabel01 的虛擬機器角色。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-115">In this case, the following command will create a virtual machine role with the name ContosoVMRole01, label ContosoVMRoleLabel01.</span></span>
<span data-ttu-id="7d5ae-116">請注意，這裡使用的資源定義必須透過 PowerShell 手動建立。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-116">Note that the resource definition being used here has to be manually created though PowerShell.</span></span>

## <span data-ttu-id="7d5ae-117">參數</span><span class="sxs-lookup"><span data-stu-id="7d5ae-117">PARAMETERS</span></span>

### <span data-ttu-id="7d5ae-118">-CloudService</span><span class="sxs-lookup"><span data-stu-id="7d5ae-118">-CloudService</span></span>
<span data-ttu-id="7d5ae-119">指定虛擬機器角色的雲端服務。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-119">Specifies a cloud service for the virtual machine role.</span></span>

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5ae-120">-標籤</span><span class="sxs-lookup"><span data-stu-id="7d5ae-120">-Label</span></span>
<span data-ttu-id="7d5ae-121">指定虛擬機器角色的標籤。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-121">Specifies a label for the virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5ae-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d5ae-122">-Name</span></span>
<span data-ttu-id="7d5ae-123">指定虛擬機器角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-123">Specifies a name for the virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5ae-124">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7d5ae-124">-Profile</span></span>
<span data-ttu-id="7d5ae-125">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7d5ae-126">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7d5ae-127">-ResourceDefinition</span><span class="sxs-lookup"><span data-stu-id="7d5ae-127">-ResourceDefinition</span></span>
<span data-ttu-id="7d5ae-128">指定虛擬機器角色的資源定義。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-128">Specifies a resource definition for the virtual machine role.</span></span>

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d5ae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d5ae-129">CommonParameters</span></span>
<span data-ttu-id="7d5ae-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d5ae-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d5ae-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d5ae-132">輸入</span><span class="sxs-lookup"><span data-stu-id="7d5ae-132">INPUTS</span></span>

## <span data-ttu-id="7d5ae-133">輸出</span><span class="sxs-lookup"><span data-stu-id="7d5ae-133">OUTPUTS</span></span>

## <span data-ttu-id="7d5ae-134">筆記</span><span class="sxs-lookup"><span data-stu-id="7d5ae-134">NOTES</span></span>

## <span data-ttu-id="7d5ae-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d5ae-135">RELATED LINKS</span></span>

[<span data-ttu-id="7d5ae-136">WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7d5ae-136">Get-WAPackVMRole</span></span>](./Get-WAPackVMRole.md)

[<span data-ttu-id="7d5ae-137">移除-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7d5ae-137">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="7d5ae-138">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="7d5ae-138">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


