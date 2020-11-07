---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968846"
---
# <span data-ttu-id="23db4-101">New-WAPackQuickVM</span><span class="sxs-lookup"><span data-stu-id="23db4-101">New-WAPackQuickVM</span></span>

## <span data-ttu-id="23db4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="23db4-102">SYNOPSIS</span></span>
<span data-ttu-id="23db4-103">根據範本建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="23db4-103">Creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="23db4-104">句法</span><span class="sxs-lookup"><span data-stu-id="23db4-104">SYNTAX</span></span>

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="23db4-105">說明</span><span class="sxs-lookup"><span data-stu-id="23db4-105">DESCRIPTION</span></span>
<span data-ttu-id="23db4-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="23db4-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="23db4-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23db4-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="23db4-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="23db4-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="23db4-109">**新的-WAPackQuickVM** Cmdlet 會根據範本建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="23db4-109">The **New-WAPackQuickVM** cmdlet creates a virtual machine based on a template.</span></span>

## <span data-ttu-id="23db4-110">示例</span><span class="sxs-lookup"><span data-stu-id="23db4-110">EXAMPLES</span></span>

### <span data-ttu-id="23db4-111">範例1：根據範本建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="23db4-111">Example 1: Create a virtual machine based on a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

<span data-ttu-id="23db4-112">第一個命令會建立一個 **PSCredential** 物件，然後將它儲存在 $Credentials 變數中。</span><span class="sxs-lookup"><span data-stu-id="23db4-112">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="23db4-113">此 Cmdlet 會提示您輸入帳戶和密碼。</span><span class="sxs-lookup"><span data-stu-id="23db4-113">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="23db4-114">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="23db4-114">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="23db4-115">第二個命令會使用 **WAPackVMTemplate** Cmdlet 取得範本。</span><span class="sxs-lookup"><span data-stu-id="23db4-115">The second command gets a template by using the **Get-WAPackVMTemplate** cmdlet.</span></span>
<span data-ttu-id="23db4-116">該命令會指定範本的識別碼。</span><span class="sxs-lookup"><span data-stu-id="23db4-116">The command specifies the ID of a template.</span></span>
<span data-ttu-id="23db4-117">該命令會將範本物件儲存在 $TemplateID 變數中。</span><span class="sxs-lookup"><span data-stu-id="23db4-117">The command stores the template object in the $TemplateID variable.</span></span>

<span data-ttu-id="23db4-118">最後一個命令會建立名為 VirtualMachine023 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="23db4-118">The final command creates a virtual machine named VirtualMachine023.</span></span>
<span data-ttu-id="23db4-119">命令會以儲存在 $TemplateId 的範本為基礎。</span><span class="sxs-lookup"><span data-stu-id="23db4-119">The command bases the virtual machine on the template stored in $TemplateId.</span></span>

## <span data-ttu-id="23db4-120">參數</span><span class="sxs-lookup"><span data-stu-id="23db4-120">PARAMETERS</span></span>

### <span data-ttu-id="23db4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="23db4-121">-Name</span></span>
<span data-ttu-id="23db4-122">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="23db4-122">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="23db4-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="23db4-123">-Profile</span></span>
<span data-ttu-id="23db4-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="23db4-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="23db4-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="23db4-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="23db4-126">-範本</span><span class="sxs-lookup"><span data-stu-id="23db4-126">-Template</span></span>
<span data-ttu-id="23db4-127">指定範本。</span><span class="sxs-lookup"><span data-stu-id="23db4-127">Specifies a template.</span></span>
<span data-ttu-id="23db4-128">這個 Cmdlet 會根據您指定的範本建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="23db4-128">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="23db4-129">若要取得範本物件，請使用 **WAPackVMTemplate** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23db4-129">To obtain a template object, use the **Get-WAPackVMTemplate** cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23db4-130">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="23db4-130">-VMCredential</span></span>
<span data-ttu-id="23db4-131">指定本機系統管理員帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="23db4-131">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="23db4-132">若要取得 **PSCredential** 物件，請使用 **取得認證** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="23db4-132">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="23db4-133">如需詳細資訊，請輸入 `Get-Help Get-Credential` 。</span><span class="sxs-lookup"><span data-stu-id="23db4-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23db4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23db4-134">CommonParameters</span></span>
<span data-ttu-id="23db4-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="23db4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23db4-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="23db4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23db4-137">輸入</span><span class="sxs-lookup"><span data-stu-id="23db4-137">INPUTS</span></span>

## <span data-ttu-id="23db4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="23db4-138">OUTPUTS</span></span>

## <span data-ttu-id="23db4-139">筆記</span><span class="sxs-lookup"><span data-stu-id="23db4-139">NOTES</span></span>

## <span data-ttu-id="23db4-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="23db4-140">RELATED LINKS</span></span>

[<span data-ttu-id="23db4-141">新-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="23db4-141">New-WAPackVM</span></span>](./New-WAPackVM.md)

[<span data-ttu-id="23db4-142">WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="23db4-142">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)


