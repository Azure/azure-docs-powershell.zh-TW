---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967434"
---
# <span data-ttu-id="e9550-101">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="e9550-101">New-AzureSBNamespace</span></span>

## <span data-ttu-id="e9550-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9550-102">SYNOPSIS</span></span>
<span data-ttu-id="e9550-103">建立命名空間。</span><span class="sxs-lookup"><span data-stu-id="e9550-103">Creates a namespace.</span></span>

## <span data-ttu-id="e9550-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9550-104">SYNTAX</span></span>

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e9550-105">說明</span><span class="sxs-lookup"><span data-stu-id="e9550-105">DESCRIPTION</span></span>
<span data-ttu-id="e9550-106">本主題描述 Microsoft Azure PowerShell 模組的0.8.10 版本中的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9550-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e9550-107">若要取得您正在使用的模組版本，請在 Azure PowerShell 主控台輸入 `(Get-Module -Name Azure).Version` 。</span><span class="sxs-lookup"><span data-stu-id="e9550-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e9550-108">**新的-AzureSBNamespace** Cmdlet 會建立服務命名空間，以搭配 Azure 中的服務匯流排使用。</span><span class="sxs-lookup"><span data-stu-id="e9550-108">The **New-AzureSBNamespace** cmdlet creates a service namespace for use with Service Bus in Azure.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="e9550-109">示例</span><span class="sxs-lookup"><span data-stu-id="e9550-109">EXAMPLES</span></span>

### <span data-ttu-id="e9550-110">範例1：建立服務命名空間</span><span class="sxs-lookup"><span data-stu-id="e9550-110">Example 1: Create a service namespace</span></span>
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

<span data-ttu-id="e9550-111">這個範例會建立一個服務命名空間，以搭配 Azure 中的服務匯流排使用。</span><span class="sxs-lookup"><span data-stu-id="e9550-111">The examples create a service namespace for use with Service Bus in Azure.</span></span>
<span data-ttu-id="e9550-112">兩個範例都包含所需的參數值，但只有先包含參數名稱。</span><span class="sxs-lookup"><span data-stu-id="e9550-112">Both examples include the required parameter values, but only the first includes the parameter names.</span></span>
<span data-ttu-id="e9550-113">您可以使用第二個範例，因為兩個參數都是位置，而它們的值會依所需順序提供。</span><span class="sxs-lookup"><span data-stu-id="e9550-113">The second example can be used because both parameters are positional and their values are given in the required order.</span></span>

## <span data-ttu-id="e9550-114">參數</span><span class="sxs-lookup"><span data-stu-id="e9550-114">PARAMETERS</span></span>

### <span data-ttu-id="e9550-115">-CreateACSNamespace</span><span class="sxs-lookup"><span data-stu-id="e9550-115">-CreateACSNamespace</span></span>
<span data-ttu-id="e9550-116">指定除了服務命名空間之外，是否要建立關聯的 ACS 命名空間。</span><span class="sxs-lookup"><span data-stu-id="e9550-116">Specifies whether to create an associated ACS namespace in addition to the service namespace.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9550-117">-位置</span><span class="sxs-lookup"><span data-stu-id="e9550-117">-Location</span></span>
<span data-ttu-id="e9550-118">指定新命名空間的區域。</span><span class="sxs-lookup"><span data-stu-id="e9550-118">Specifies a region for the new namespace.</span></span>

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

### <span data-ttu-id="e9550-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9550-119">-Name</span></span>
<span data-ttu-id="e9550-120">指定新命名空間的名稱。</span><span class="sxs-lookup"><span data-stu-id="e9550-120">Specifies a name for the new namespace.</span></span>

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

### <span data-ttu-id="e9550-121">-NamespaceType</span><span class="sxs-lookup"><span data-stu-id="e9550-121">-NamespaceType</span></span>
<span data-ttu-id="e9550-122">指定是否要將命名空間用於訊息或通知中樞。</span><span class="sxs-lookup"><span data-stu-id="e9550-122">Specify a whether to use the namespace for Messaging or Notification Hubs.</span></span>

```yaml
Type: NamespaceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9550-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="e9550-123">-Profile</span></span>
<span data-ttu-id="e9550-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="e9550-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e9550-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="e9550-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e9550-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9550-126">CommonParameters</span></span>
<span data-ttu-id="e9550-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9550-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9550-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e9550-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9550-129">輸入</span><span class="sxs-lookup"><span data-stu-id="e9550-129">INPUTS</span></span>

## <span data-ttu-id="e9550-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e9550-130">OUTPUTS</span></span>

## <span data-ttu-id="e9550-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e9550-131">NOTES</span></span>

## <span data-ttu-id="e9550-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9550-132">RELATED LINKS</span></span>

[<span data-ttu-id="e9550-133">移除-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="e9550-133">Remove-AzureSBNamespace</span></span>](./Remove-AzureSBNamespace.md)


