---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968860"
---
# <span data-ttu-id="943e5-101">Get-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="943e5-101">Get-WAPackVMRole</span></span>

## <span data-ttu-id="943e5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="943e5-102">SYNOPSIS</span></span>

## <span data-ttu-id="943e5-103">句法</span><span class="sxs-lookup"><span data-stu-id="943e5-103">SYNTAX</span></span>

### <span data-ttu-id="943e5-104">空白 (預設) </span><span class="sxs-lookup"><span data-stu-id="943e5-104">Empty (Default)</span></span>
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="943e5-105">FromName</span><span class="sxs-lookup"><span data-stu-id="943e5-105">FromName</span></span>
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="943e5-106">FromCloudService</span><span class="sxs-lookup"><span data-stu-id="943e5-106">FromCloudService</span></span>
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="943e5-107">說明</span><span class="sxs-lookup"><span data-stu-id="943e5-107">DESCRIPTION</span></span>
<span data-ttu-id="943e5-108">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="943e5-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="943e5-109">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="943e5-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="943e5-110">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="943e5-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="943e5-111">示例</span><span class="sxs-lookup"><span data-stu-id="943e5-111">EXAMPLES</span></span>

### <span data-ttu-id="943e5-112">範例1：取得透過入口網站建立 (虛擬電腦角色) </span><span class="sxs-lookup"><span data-stu-id="943e5-112">Example 1: Get a virtual machine role (created through the portal)</span></span>
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

<span data-ttu-id="943e5-113">這個命令會取得已透過名為 ContosoVMRole01 的入口網站建立的虛擬機器角色。</span><span class="sxs-lookup"><span data-stu-id="943e5-113">This command gets a virtual machine role which has been created through the portal named ContosoVMRole01.</span></span>

### <span data-ttu-id="943e5-114">範例2：使用名稱和雲端服務名稱取得虛擬機器角色</span><span class="sxs-lookup"><span data-stu-id="943e5-114">Example 2: Get a virtual machine role by using a name and a cloud service name</span></span>
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

<span data-ttu-id="943e5-115">這個命令會取得一個名為 ContosoVMRole02 的虛擬電腦角色，該角色在名為 ContosoCloudService01 的雲端服務上。</span><span class="sxs-lookup"><span data-stu-id="943e5-115">This command gets a virtual machine role named ContosoVMRole02 which stand on a cloud service named ContosoCloudService01.</span></span>

### <span data-ttu-id="943e5-116">範例3：取得所有虛擬機器角色</span><span class="sxs-lookup"><span data-stu-id="943e5-116">Example 3: Get all virtual machine role</span></span>
```
PS C:\> Get-WAPackVMRole
```

<span data-ttu-id="943e5-117">這個命令會取得所有現有的虛擬機器角色。</span><span class="sxs-lookup"><span data-stu-id="943e5-117">This command gets all existing virtual machine role.</span></span>

## <span data-ttu-id="943e5-118">參數</span><span class="sxs-lookup"><span data-stu-id="943e5-118">PARAMETERS</span></span>

### <span data-ttu-id="943e5-119">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="943e5-119">-CloudServiceName</span></span>
<span data-ttu-id="943e5-120">指定虛擬機器角色的雲端服務名稱。</span><span class="sxs-lookup"><span data-stu-id="943e5-120">Specifies the cloud service name of virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="943e5-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="943e5-121">-Name</span></span>
<span data-ttu-id="943e5-122">指定虛擬機器角色的名稱。</span><span class="sxs-lookup"><span data-stu-id="943e5-122">Specifies the name of a virtual machine role.</span></span>

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="943e5-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="943e5-123">-Profile</span></span>
<span data-ttu-id="943e5-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="943e5-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="943e5-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="943e5-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="943e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="943e5-126">CommonParameters</span></span>
<span data-ttu-id="943e5-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="943e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="943e5-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="943e5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="943e5-129">輸入</span><span class="sxs-lookup"><span data-stu-id="943e5-129">INPUTS</span></span>

## <span data-ttu-id="943e5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="943e5-130">OUTPUTS</span></span>

## <span data-ttu-id="943e5-131">筆記</span><span class="sxs-lookup"><span data-stu-id="943e5-131">NOTES</span></span>

## <span data-ttu-id="943e5-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="943e5-132">RELATED LINKS</span></span>

[<span data-ttu-id="943e5-133">新-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="943e5-133">New-WAPackVMRole</span></span>](./New-WAPackVMRole.md)

[<span data-ttu-id="943e5-134">移除-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="943e5-134">Remove-WAPackVMRole</span></span>](./Remove-WAPackVMRole.md)

[<span data-ttu-id="943e5-135">Set-WAPackVMRole</span><span class="sxs-lookup"><span data-stu-id="943e5-135">Set-WAPackVMRole</span></span>](./Set-WAPackVMRole.md)


