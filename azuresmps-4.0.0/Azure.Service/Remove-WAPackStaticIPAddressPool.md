---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CE618AD2-7E28-4012-BF3C-B932B95FFDD5
online version: ''
schema: 2.0.0
ms.openlocfilehash: a07358c37bf30e8d5fc3040cdfd174b800df96e4
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/08/2020
ms.locfileid: "93968858"
---
# <span data-ttu-id="7f7fc-101">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="7f7fc-101">Remove-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="7f7fc-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f7fc-102">SYNOPSIS</span></span>
<span data-ttu-id="7f7fc-103">移除靜態 IP 位址池物件。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-103">Removes static IP address pool objects.</span></span>

## <span data-ttu-id="7f7fc-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f7fc-104">SYNTAX</span></span>

```
Remove-WAPackStaticIPAddressPool -StaticIPAddressPool <StaticIPAddressPool> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7f7fc-105">說明</span><span class="sxs-lookup"><span data-stu-id="7f7fc-105">DESCRIPTION</span></span>
<span data-ttu-id="7f7fc-106">這些主題已棄用，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="7f7fc-107">本主題描述 Microsoft Azure PowerShell 模組的0.8.1 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7f7fc-108">若要找出您正在使用的模組版本，請從 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7f7fc-109">**WAPackStaticIPAddressPool** Cmdlet 會移除靜態 IP 位址池物件。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-109">The **Remove-WAPackStaticIPAddressPool** cmdlet removes static IP address pool objects.</span></span>

## <span data-ttu-id="7f7fc-110">示例</span><span class="sxs-lookup"><span data-stu-id="7f7fc-110">EXAMPLES</span></span>

### <span data-ttu-id="7f7fc-111">範例1：移除靜態 IP 位址池</span><span class="sxs-lookup"><span data-stu-id="7f7fc-111">Example 1: Remove a static IP address pool</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool01"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool
```

<span data-ttu-id="7f7fc-112">第一個命令會使用 **WAPackStaticIPAddressPool** Cmdlet 取得名為 ContosoStaticIPAddressPool01 的靜態 IP 位址池，然後將該物件儲存在 $StaticIPAddressPool 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-112">The first command gets the static IP address pool named ContosoStaticIPAddressPool01 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $StaticIPAddressPool variable.</span></span>

<span data-ttu-id="7f7fc-113">第二個命令會移除 $StaticIPAddressPool 中儲存的靜態 IP 位址池。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-113">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="7f7fc-114">命令會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="7f7fc-115">範例2：移除靜態 IP 位址池而不進行確認</span><span class="sxs-lookup"><span data-stu-id="7f7fc-115">Example 2: Remove a static IP address pool without confirmation</span></span>
```
PS C:\> $StaticIPAddressPool = Get-WAPackStaticIPAddressPool -Name "ContosoStaticIPAddressPool02"
PS C:\> Remove-WAPackStaticIPAddressPool -StaticIPAddressPool $StaticIPAddressPool -Force
```

<span data-ttu-id="7f7fc-116">第一個命令會使用 **WAPackStaticIPAddressPool** Cmdlet 取得名為 ContosoStaticIPAddressPool02 的靜態 IP 位址池，然後將該物件儲存在 $ StaticIPAddressPool 變數中。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-116">The first command gets the static IP address pool named ContosoStaticIPAddressPool02 by using the **Get-WAPackStaticIPAddressPool** cmdlet, and then stores that object in the $ StaticIPAddressPool variable.</span></span>

<span data-ttu-id="7f7fc-117">第二個命令會移除 $StaticIPAddressPool 中儲存的靜態 IP 位址池。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-117">The second command removes the static IP address pool stored in $StaticIPAddressPool.</span></span>
<span data-ttu-id="7f7fc-118">這個命令包含 *Force* 參數。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-118">This command includes the *Force* parameter.</span></span>
<span data-ttu-id="7f7fc-119">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-119">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="7f7fc-120">參數</span><span class="sxs-lookup"><span data-stu-id="7f7fc-120">PARAMETERS</span></span>

### <span data-ttu-id="7f7fc-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7f7fc-121">-Force</span></span>
<span data-ttu-id="7f7fc-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7f7fc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f7fc-123">-PassThru</span></span>
<span data-ttu-id="7f7fc-124">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7f7fc-125">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7f7fc-126">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7f7fc-126">-Profile</span></span>
<span data-ttu-id="7f7fc-127">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7f7fc-128">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7f7fc-129">-StaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="7f7fc-129">-StaticIPAddressPool</span></span>
<span data-ttu-id="7f7fc-130">指定 StaticIPAddressPool。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-130">Specifies a StaticIPAddressPool.</span></span>
<span data-ttu-id="7f7fc-131">若要取得靜態 IP 位址池，請使用 **WAPackStaticIPAddressPool** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-131">To obtain a static IP address pool, use the **Get-WAPackStaticIPAddressPool** cmdlet.</span></span>

```yaml
Type: StaticIPAddressPool
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f7fc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f7fc-132">CommonParameters</span></span>
<span data-ttu-id="7f7fc-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f7fc-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7f7fc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f7fc-135">輸入</span><span class="sxs-lookup"><span data-stu-id="7f7fc-135">INPUTS</span></span>

## <span data-ttu-id="7f7fc-136">輸出</span><span class="sxs-lookup"><span data-stu-id="7f7fc-136">OUTPUTS</span></span>

## <span data-ttu-id="7f7fc-137">筆記</span><span class="sxs-lookup"><span data-stu-id="7f7fc-137">NOTES</span></span>

## <span data-ttu-id="7f7fc-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f7fc-138">RELATED LINKS</span></span>

[<span data-ttu-id="7f7fc-139">WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="7f7fc-139">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="7f7fc-140">移除-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="7f7fc-140">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


