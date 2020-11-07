---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1D433BD2-4604-474B-A2DA-BC80EE935E5C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ffbe5ae961c1733be68c902a9657b200cba0a5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967059"
---
# <span data-ttu-id="05f4b-101">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="05f4b-101">Get-AzureSBNamespace</span></span>

## <span data-ttu-id="05f4b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="05f4b-103">取得命名空間。</span><span class="sxs-lookup"><span data-stu-id="05f4b-103">Gets the namespace.</span></span>


## <span data-ttu-id="05f4b-104">句法</span><span class="sxs-lookup"><span data-stu-id="05f4b-104">SYNTAX</span></span>

```
Get-AzureSBNamespace [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="05f4b-105">說明</span><span class="sxs-lookup"><span data-stu-id="05f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="05f4b-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05f4b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="05f4b-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="05f4b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="05f4b-108">**AzureSBNamespace** Cmdlet 會傳回與目前訂閱相關聯的服務匯流排服務命名空間。</span><span class="sxs-lookup"><span data-stu-id="05f4b-108">The **Get-AzureSBNamespace** cmdlet returns the Service Bus service namespaces associated with the current subscription.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="05f4b-109">示例</span><span class="sxs-lookup"><span data-stu-id="05f4b-109">EXAMPLES</span></span>

### <span data-ttu-id="05f4b-110">範例1：取得服務匯流排命名空間</span><span class="sxs-lookup"><span data-stu-id="05f4b-110">Example 1: Get the Service Bus namespace</span></span>
```
PS C:\> Get-AzureSBNamespace
```

<span data-ttu-id="05f4b-111">這個範例會取得與目前訂閱相關聯的服務匯流排服務命名空間。</span><span class="sxs-lookup"><span data-stu-id="05f4b-111">This example gets the Service Bus service namespaces associated with the current subscription.</span></span>

## <span data-ttu-id="05f4b-112">參數</span><span class="sxs-lookup"><span data-stu-id="05f4b-112">PARAMETERS</span></span>

### <span data-ttu-id="05f4b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="05f4b-113">-Name</span></span>
<span data-ttu-id="05f4b-114">指定要尋找的服務匯流排命名空間名稱。</span><span class="sxs-lookup"><span data-stu-id="05f4b-114">Specifies the name of a Service Bus namespace to look for.</span></span>

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

### <span data-ttu-id="05f4b-115">-設定檔</span><span class="sxs-lookup"><span data-stu-id="05f4b-115">-Profile</span></span>
<span data-ttu-id="05f4b-116">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="05f4b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05f4b-117">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="05f4b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05f4b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05f4b-118">CommonParameters</span></span>
<span data-ttu-id="05f4b-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05f4b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05f4b-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05f4b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05f4b-121">輸入</span><span class="sxs-lookup"><span data-stu-id="05f4b-121">INPUTS</span></span>

## <span data-ttu-id="05f4b-122">輸出</span><span class="sxs-lookup"><span data-stu-id="05f4b-122">OUTPUTS</span></span>

## <span data-ttu-id="05f4b-123">筆記</span><span class="sxs-lookup"><span data-stu-id="05f4b-123">NOTES</span></span>

## <span data-ttu-id="05f4b-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="05f4b-124">RELATED LINKS</span></span>

[<span data-ttu-id="05f4b-125">AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="05f4b-125">Get-AzureSBLocation</span></span>](./Get-AzureSBLocation.md)


