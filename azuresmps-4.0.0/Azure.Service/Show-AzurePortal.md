---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7ABEC06E-1046-401E-B4A1-902FC3EED867
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0f0ff81fc38916adeedbb495117a8b27a1f88fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967394"
---
# <span data-ttu-id="66add-101">Show-AzurePortal</span><span class="sxs-lookup"><span data-stu-id="66add-101">Show-AzurePortal</span></span>

## <span data-ttu-id="66add-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66add-102">SYNOPSIS</span></span>
<span data-ttu-id="66add-103">顯示 Azure 管理入口網站。</span><span class="sxs-lookup"><span data-stu-id="66add-103">Show the Azure Management Portal.</span></span>

## <span data-ttu-id="66add-104">句法</span><span class="sxs-lookup"><span data-stu-id="66add-104">SYNTAX</span></span>

```
Show-AzurePortal [-Name <String>] [-Realm <String>] [-Environment <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="66add-105">說明</span><span class="sxs-lookup"><span data-stu-id="66add-105">DESCRIPTION</span></span>
<span data-ttu-id="66add-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66add-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="66add-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="66add-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="66add-108">**AzurePortal** Cmdlet 會顯示 Azure 管理入口網站。</span><span class="sxs-lookup"><span data-stu-id="66add-108">The **Show-AzurePortal** cmdlet shows the Azure Management Portal.</span></span>

## <span data-ttu-id="66add-109">示例</span><span class="sxs-lookup"><span data-stu-id="66add-109">EXAMPLES</span></span>

### <span data-ttu-id="66add-110">範例1：顯示網站的相關資訊</span><span class="sxs-lookup"><span data-stu-id="66add-110">Example 1: Show information about a web site</span></span>
```
PS C:\> Show-AzurePortal -Name mySite
```

<span data-ttu-id="66add-111">這個範例會在 Azure 入口網站上開啟瀏覽器，顯示名為「我的網站」網站的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="66add-111">This example opens a browser on the Azure portal, showing information about a web site named mySite.</span></span>

## <span data-ttu-id="66add-112">參數</span><span class="sxs-lookup"><span data-stu-id="66add-112">PARAMETERS</span></span>

### <span data-ttu-id="66add-113">-環境</span><span class="sxs-lookup"><span data-stu-id="66add-113">-Environment</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66add-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="66add-114">-Name</span></span>
<span data-ttu-id="66add-115">指定要顯示在入口網站中的網站名稱。</span><span class="sxs-lookup"><span data-stu-id="66add-115">Specifies the name of the website to show in the portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66add-116">-設定檔</span><span class="sxs-lookup"><span data-stu-id="66add-116">-Profile</span></span>
<span data-ttu-id="66add-117">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="66add-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="66add-118">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="66add-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66add-119">-領域</span><span class="sxs-lookup"><span data-stu-id="66add-119">-Realm</span></span>
<span data-ttu-id="66add-120">指定顯示 Azure 入口網站時用於同盟驗證的組織識別碼。</span><span class="sxs-lookup"><span data-stu-id="66add-120">Specifies the organization ID to use for federated authentication when displaying the Azure Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66add-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66add-121">CommonParameters</span></span>
<span data-ttu-id="66add-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66add-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66add-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66add-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66add-124">輸入</span><span class="sxs-lookup"><span data-stu-id="66add-124">INPUTS</span></span>

## <span data-ttu-id="66add-125">輸出</span><span class="sxs-lookup"><span data-stu-id="66add-125">OUTPUTS</span></span>

## <span data-ttu-id="66add-126">筆記</span><span class="sxs-lookup"><span data-stu-id="66add-126">NOTES</span></span>

## <span data-ttu-id="66add-127">相關連結</span><span class="sxs-lookup"><span data-stu-id="66add-127">RELATED LINKS</span></span>

[<span data-ttu-id="66add-128">顯示-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="66add-128">Show-AzureWebsite</span></span>](./Show-AzureWebsite.md)


