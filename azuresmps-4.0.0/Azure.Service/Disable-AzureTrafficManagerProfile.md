---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967139"
---
# <span data-ttu-id="0d707-101">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0d707-101">Disable-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="0d707-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d707-102">SYNOPSIS</span></span>
<span data-ttu-id="0d707-103">停用流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="0d707-103">Disables a Traffic Manager profile.</span></span>

## <span data-ttu-id="0d707-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d707-104">SYNTAX</span></span>

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0d707-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d707-105">DESCRIPTION</span></span>
<span data-ttu-id="0d707-106">**Disable AzureTrafficManagerProfile** Cmdlet 會停用 Microsoft Azure 流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="0d707-106">The **Disable-AzureTrafficManagerProfile** cmdlet disables a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="0d707-107">您可以使用 *PassThru* 參數來顯示操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="0d707-107">You can use the *PassThru* parameter to display whether the operation succeeds.</span></span>

## <span data-ttu-id="0d707-108">示例</span><span class="sxs-lookup"><span data-stu-id="0d707-108">EXAMPLES</span></span>

### <span data-ttu-id="0d707-109">範例1：停用流量管理器設定檔並顯示結果</span><span class="sxs-lookup"><span data-stu-id="0d707-109">Example 1: Disable a Traffic Manager profile and display the results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

<span data-ttu-id="0d707-110">這個命令會停用名為 MyProfile 的流量管理器設定檔。</span><span class="sxs-lookup"><span data-stu-id="0d707-110">This command disables the Traffic Manager profile named MyProfile.</span></span>
<span data-ttu-id="0d707-111">命令會指定 *PassThru* 參數，以顯示命令是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="0d707-111">The command specifies the *PassThru* parameter to display whether the command succeeded.</span></span>

### <span data-ttu-id="0d707-112">範例2：停用流量管理器設定檔，且不顯示任何結果</span><span class="sxs-lookup"><span data-stu-id="0d707-112">Example 2: Disable a Traffic Manager profile and display no results</span></span>
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

<span data-ttu-id="0d707-113">這個命令會停用名為 MyProfile 的流量管理器設定檔，但不會顯示命令是否已成功完成。</span><span class="sxs-lookup"><span data-stu-id="0d707-113">This command disables the Traffic Manager profile named MyProfile but does not display whether the command succeeded.</span></span>

## <span data-ttu-id="0d707-114">參數</span><span class="sxs-lookup"><span data-stu-id="0d707-114">PARAMETERS</span></span>

### <span data-ttu-id="0d707-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d707-115">-Name</span></span>
<span data-ttu-id="0d707-116">指定要停用之流量管理器設定檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d707-116">Specifies the name of the Traffic Manager profile to disable.</span></span>

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

### <span data-ttu-id="0d707-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d707-117">-PassThru</span></span>
<span data-ttu-id="0d707-118">如果操作成功，則傳回 $True;否則，請 $False。</span><span class="sxs-lookup"><span data-stu-id="0d707-118">Returns $True if the operation succeeded; otherwise, $False.</span></span>
<span data-ttu-id="0d707-119">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="0d707-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d707-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="0d707-120">-Profile</span></span>
<span data-ttu-id="0d707-121">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="0d707-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0d707-122">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="0d707-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0d707-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d707-123">CommonParameters</span></span>
<span data-ttu-id="0d707-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d707-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d707-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d707-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d707-126">輸入</span><span class="sxs-lookup"><span data-stu-id="0d707-126">INPUTS</span></span>

## <span data-ttu-id="0d707-127">輸出</span><span class="sxs-lookup"><span data-stu-id="0d707-127">OUTPUTS</span></span>

### <span data-ttu-id="0d707-128">System.object</span><span class="sxs-lookup"><span data-stu-id="0d707-128">System.Boolean</span></span>
<span data-ttu-id="0d707-129">這個 Cmdlet 會產生 $True 或 $False。</span><span class="sxs-lookup"><span data-stu-id="0d707-129">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="0d707-130">如果操作成功，且您指定 *PassThru* 參數，則此 Cmdlet 會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="0d707-130">If the operation is successful and if you specify the *PassThru* parameter, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="0d707-131">筆記</span><span class="sxs-lookup"><span data-stu-id="0d707-131">NOTES</span></span>

## <span data-ttu-id="0d707-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d707-132">RELATED LINKS</span></span>

[<span data-ttu-id="0d707-133">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0d707-133">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="0d707-134">AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0d707-134">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="0d707-135">新-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0d707-135">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="0d707-136">移除-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0d707-136">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="0d707-137">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0d707-137">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


