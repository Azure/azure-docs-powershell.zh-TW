---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D927B159-AD68-4071-ADE3-FA2430750D72
online version: ''
schema: 2.0.0
ms.openlocfilehash: 001466cb00ad15f1cbfef6dcf9fd3ce9b931109b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967901"
---
# <span data-ttu-id="a9603-101">Remove-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="a9603-101">Remove-AzureStoreAddOn</span></span>

## <span data-ttu-id="a9603-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a9603-102">SYNOPSIS</span></span>
<span data-ttu-id="a9603-103">移除現有的附加元件實例。</span><span class="sxs-lookup"><span data-stu-id="a9603-103">Removes an existing add-on instance.</span></span>

## <span data-ttu-id="a9603-104">句法</span><span class="sxs-lookup"><span data-stu-id="a9603-104">SYNTAX</span></span>

```
Remove-AzureStoreAddOn -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a9603-105">說明</span><span class="sxs-lookup"><span data-stu-id="a9603-105">DESCRIPTION</span></span>
<span data-ttu-id="a9603-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a9603-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a9603-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="a9603-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a9603-108">從目前的訂閱中移除現有的附加元件實例。</span><span class="sxs-lookup"><span data-stu-id="a9603-108">Removes an existing add-on instance from the current subscription.</span></span>

## <span data-ttu-id="a9603-109">示例</span><span class="sxs-lookup"><span data-stu-id="a9603-109">EXAMPLES</span></span>

### <span data-ttu-id="a9603-110">範例1</span><span class="sxs-lookup"><span data-stu-id="a9603-110">Example 1</span></span>
```
PS C:\> Remove-AzureStoreAddOn MyAddOn
```

<span data-ttu-id="a9603-111">這個範例會從目前的訂閱中移除一個名為 MyAddOn 的附加元件。</span><span class="sxs-lookup"><span data-stu-id="a9603-111">This example removes an add-on named MyAddOn from the current subscription.</span></span>

## <span data-ttu-id="a9603-112">參數</span><span class="sxs-lookup"><span data-stu-id="a9603-112">PARAMETERS</span></span>

### <span data-ttu-id="a9603-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="a9603-113">-Name</span></span>
<span data-ttu-id="a9603-114">指定要移除的附加元件實例的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9603-114">Specifies the name of the add-on instance to remove.</span></span>

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

### <span data-ttu-id="a9603-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9603-115">-PassThru</span></span>
<span data-ttu-id="a9603-116">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="a9603-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a9603-117">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="a9603-117">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9603-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a9603-118">-Profile</span></span>
<span data-ttu-id="a9603-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a9603-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a9603-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a9603-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a9603-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9603-121">CommonParameters</span></span>
<span data-ttu-id="a9603-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a9603-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9603-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a9603-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9603-124">輸入</span><span class="sxs-lookup"><span data-stu-id="a9603-124">INPUTS</span></span>

## <span data-ttu-id="a9603-125">輸出</span><span class="sxs-lookup"><span data-stu-id="a9603-125">OUTPUTS</span></span>

## <span data-ttu-id="a9603-126">筆記</span><span class="sxs-lookup"><span data-stu-id="a9603-126">NOTES</span></span>

## <span data-ttu-id="a9603-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="a9603-127">RELATED LINKS</span></span>

[<span data-ttu-id="a9603-128">AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="a9603-128">Get-AzureStoreAddOn</span></span>](./Get-AzureStoreAddOn.md)

[<span data-ttu-id="a9603-129">新-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="a9603-129">New-AzureStoreAddOn</span></span>](./New-AzureStoreAddOn.md)

[<span data-ttu-id="a9603-130">Set-AzureStoreAddOn</span><span class="sxs-lookup"><span data-stu-id="a9603-130">Set-AzureStoreAddOn</span></span>](./Set-AzureStoreAddOn.md)


