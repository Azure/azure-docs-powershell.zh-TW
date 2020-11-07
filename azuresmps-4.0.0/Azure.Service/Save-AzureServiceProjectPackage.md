---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9445B7FA-FC72-4F71-BD44-8AA55BE9BA0E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d2a3dbabb5bbe78ed571806aa69b9d79d4782b3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966906"
---
# <span data-ttu-id="ff6ed-101">Save-AzureServiceProjectPackage</span><span class="sxs-lookup"><span data-stu-id="ff6ed-101">Save-AzureServiceProjectPackage</span></span>

## <span data-ttu-id="ff6ed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff6ed-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6ed-103">將服務專案封裝到 Azure 雲端套件中。</span><span class="sxs-lookup"><span data-stu-id="ff6ed-103">Packages the service project into Azure cloud package.</span></span>

## <span data-ttu-id="ff6ed-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff6ed-104">SYNTAX</span></span>

```
Save-AzureServiceProjectPackage [-Local] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ff6ed-105">說明</span><span class="sxs-lookup"><span data-stu-id="ff6ed-105">DESCRIPTION</span></span>
<span data-ttu-id="ff6ed-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff6ed-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ff6ed-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="ff6ed-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ff6ed-108">**AzureServiceProjectPackage** Cmdlet 會將服務專案封裝到 Azure 雲端套件中， ( \*. cspkg) 。</span><span class="sxs-lookup"><span data-stu-id="ff6ed-108">The **Save-AzureServiceProjectPackage** cmdlet packages the service project into an Azure cloud package (\*.cspkg).</span></span>

## <span data-ttu-id="ff6ed-109">示例</span><span class="sxs-lookup"><span data-stu-id="ff6ed-109">EXAMPLES</span></span>

### <span data-ttu-id="ff6ed-110">範例1：建立服務專案套件</span><span class="sxs-lookup"><span data-stu-id="ff6ed-110">Example 1: Create a service project package</span></span>
```
PS C:\> Save-AzureServiceProjectPackage
```

<span data-ttu-id="ff6ed-111">這個範例會建立名為 MyAzureServiceProject 的服務專案的 cspgk。</span><span class="sxs-lookup"><span data-stu-id="ff6ed-111">This example creates a \*.cspgk for a service project named MyAzureServiceProject.</span></span>

## <span data-ttu-id="ff6ed-112">參數</span><span class="sxs-lookup"><span data-stu-id="ff6ed-112">PARAMETERS</span></span>

### <span data-ttu-id="ff6ed-113">-本機</span><span class="sxs-lookup"><span data-stu-id="ff6ed-113">-Local</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff6ed-114">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ff6ed-114">-Profile</span></span>
<span data-ttu-id="ff6ed-115">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ff6ed-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ff6ed-116">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ff6ed-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ff6ed-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6ed-117">CommonParameters</span></span>
<span data-ttu-id="ff6ed-118">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff6ed-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6ed-119">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ff6ed-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6ed-120">輸入</span><span class="sxs-lookup"><span data-stu-id="ff6ed-120">INPUTS</span></span>

## <span data-ttu-id="ff6ed-121">輸出</span><span class="sxs-lookup"><span data-stu-id="ff6ed-121">OUTPUTS</span></span>

## <span data-ttu-id="ff6ed-122">筆記</span><span class="sxs-lookup"><span data-stu-id="ff6ed-122">NOTES</span></span>

## <span data-ttu-id="ff6ed-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff6ed-123">RELATED LINKS</span></span>

[<span data-ttu-id="ff6ed-124">發佈-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ff6ed-124">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)


