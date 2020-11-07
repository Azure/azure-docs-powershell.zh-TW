---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967664"
---
# <span data-ttu-id="47378-101">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="47378-101">New-AzureServiceProject</span></span>

## <span data-ttu-id="47378-102">摘要</span><span class="sxs-lookup"><span data-stu-id="47378-102">SYNOPSIS</span></span>
<span data-ttu-id="47378-103">為新的服務建立所需的檔案和配置。</span><span class="sxs-lookup"><span data-stu-id="47378-103">Creates the required files and configuration for a new service.</span></span>

## <span data-ttu-id="47378-104">句法</span><span class="sxs-lookup"><span data-stu-id="47378-104">SYNTAX</span></span>

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="47378-105">說明</span><span class="sxs-lookup"><span data-stu-id="47378-105">DESCRIPTION</span></span>
<span data-ttu-id="47378-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="47378-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="47378-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="47378-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="47378-108">**新的-AzureServiceProject** Cmdlet 會針對目前目錄中的新 Azure 服務建立所需的檔案和配置。</span><span class="sxs-lookup"><span data-stu-id="47378-108">The **New-AzureServiceProject** cmdlet creates the required files and configuration for a new Azure service in the current directory.</span></span>

## <span data-ttu-id="47378-109">示例</span><span class="sxs-lookup"><span data-stu-id="47378-109">EXAMPLES</span></span>

### <span data-ttu-id="47378-110">範例1：建立服務的基架</span><span class="sxs-lookup"><span data-stu-id="47378-110">Example 1: Create scaffolding for a service</span></span>
```
PS C:\> New-AzureServiceProject MyService1
```

<span data-ttu-id="47378-111">這個範例會為目前目錄中名為 MyService1 的新 Azure 服務建立基架。</span><span class="sxs-lookup"><span data-stu-id="47378-111">This example creates scaffolding for a new Azure service named MyService1 in the current directory.</span></span>

## <span data-ttu-id="47378-112">參數</span><span class="sxs-lookup"><span data-stu-id="47378-112">PARAMETERS</span></span>

### <span data-ttu-id="47378-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="47378-113">-Profile</span></span>
<span data-ttu-id="47378-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="47378-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="47378-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="47378-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="47378-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="47378-116">-ServiceName</span></span>
<span data-ttu-id="47378-117">指定服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="47378-117">Specifies the name of the service.</span></span>
<span data-ttu-id="47378-118">它會決定您服務的主機名稱的第一個區段 (例如，name.cloudapp.net) ，以及將包含您服務的目錄。</span><span class="sxs-lookup"><span data-stu-id="47378-118">It determines the first section of the hostname for your service (for example, name.cloudapp.net), and the directory that will contain your service.</span></span>
<span data-ttu-id="47378-119">名稱只能包含字母、數位和短劃線字元 ( ) 。</span><span class="sxs-lookup"><span data-stu-id="47378-119">The name can contain only letters, digits, and the dash character (-).</span></span>

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

### <span data-ttu-id="47378-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47378-120">CommonParameters</span></span>
<span data-ttu-id="47378-121">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="47378-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47378-122">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="47378-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47378-123">輸入</span><span class="sxs-lookup"><span data-stu-id="47378-123">INPUTS</span></span>

## <span data-ttu-id="47378-124">輸出</span><span class="sxs-lookup"><span data-stu-id="47378-124">OUTPUTS</span></span>

## <span data-ttu-id="47378-125">筆記</span><span class="sxs-lookup"><span data-stu-id="47378-125">NOTES</span></span>

## <span data-ttu-id="47378-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="47378-126">RELATED LINKS</span></span>

[<span data-ttu-id="47378-127">附加 AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="47378-127">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="47378-128">附加 AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="47378-128">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="47378-129">發佈-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="47378-129">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="47378-130">Set-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="47378-130">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)

[<span data-ttu-id="47378-131">Set-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="47378-131">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


