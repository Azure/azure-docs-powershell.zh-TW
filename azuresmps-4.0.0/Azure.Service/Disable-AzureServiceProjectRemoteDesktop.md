---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E735FCE5-D82F-42D0-8D74-6A568E55AC17
online version: ''
schema: 2.0.0
ms.openlocfilehash: 433a50a93f8fa8e68021d09d5c1ae464703e227c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967142"
---
# <span data-ttu-id="fc26c-101">Disable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="fc26c-101">Disable-AzureServiceProjectRemoteDesktop</span></span>

## <span data-ttu-id="fc26c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="fc26c-102">SYNOPSIS</span></span>
<span data-ttu-id="fc26c-103">停用遠端桌面電腦對雲端服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="fc26c-103">Disables Remote Desktop access to a cloud service.</span></span>

## <span data-ttu-id="fc26c-104">句法</span><span class="sxs-lookup"><span data-stu-id="fc26c-104">SYNTAX</span></span>

```
Disable-AzureServiceProjectRemoteDesktop [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fc26c-105">說明</span><span class="sxs-lookup"><span data-stu-id="fc26c-105">DESCRIPTION</span></span>
<span data-ttu-id="fc26c-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fc26c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="fc26c-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="fc26c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="fc26c-108">**Disable-AzureServiceProjectRemoteDesktop** 會停用遠端桌面對託管服務的存取權。</span><span class="sxs-lookup"><span data-stu-id="fc26c-108">The **Disable-AzureServiceProjectRemoteDesktop** disables remote desktop access to a hosted service.</span></span>
<span data-ttu-id="fc26c-109">在停用遠端桌面存取之後，您必須使用 **Publish AzureServiceProject** Cmdlet 發佈服務，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="fc26c-109">You must publish the service using the **Publish-AzureServiceProject** cmdlet after disabling Remote Desktop access for the change to take effect.</span></span>

## <span data-ttu-id="fc26c-110">示例</span><span class="sxs-lookup"><span data-stu-id="fc26c-110">EXAMPLES</span></span>

## <span data-ttu-id="fc26c-111">參數</span><span class="sxs-lookup"><span data-stu-id="fc26c-111">PARAMETERS</span></span>

### <span data-ttu-id="fc26c-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc26c-112">-PassThru</span></span>
<span data-ttu-id="fc26c-113">傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="fc26c-113">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fc26c-114">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="fc26c-114">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc26c-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="fc26c-115">-Profile</span></span>
<span data-ttu-id="fc26c-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="fc26c-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fc26c-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="fc26c-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fc26c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc26c-118">CommonParameters</span></span>
<span data-ttu-id="fc26c-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="fc26c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc26c-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="fc26c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc26c-121">輸入</span><span class="sxs-lookup"><span data-stu-id="fc26c-121">INPUTS</span></span>

## <span data-ttu-id="fc26c-122">輸出</span><span class="sxs-lookup"><span data-stu-id="fc26c-122">OUTPUTS</span></span>

## <span data-ttu-id="fc26c-123">筆記</span><span class="sxs-lookup"><span data-stu-id="fc26c-123">NOTES</span></span>

## <span data-ttu-id="fc26c-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="fc26c-124">RELATED LINKS</span></span>

[<span data-ttu-id="fc26c-125">Enable-AzureServiceProjectRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="fc26c-125">Enable-AzureServiceProjectRemoteDesktop</span></span>](./Enable-AzureServiceProjectRemoteDesktop.md)


