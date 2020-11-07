---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 636280D6-32C3-48EF-A271-A4E032F8B334
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0dab3720a4680805e16f695a1ab1b2350554e8f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967765"
---
# <span data-ttu-id="6bb17-101">Get-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="6bb17-101">Get-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="6bb17-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6bb17-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb17-103">檢索集合的一或多個已發佈 Azure RemoteApp 程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="6bb17-103">Retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="6bb17-104">句法</span><span class="sxs-lookup"><span data-stu-id="6bb17-104">SYNTAX</span></span>

### <span data-ttu-id="6bb17-105">FilterByName (預設) </span><span class="sxs-lookup"><span data-stu-id="6bb17-105">FilterByName (Default)</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-RemoteAppProgram] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="6bb17-106">FilterByAlias</span><span class="sxs-lookup"><span data-stu-id="6bb17-106">FilterByAlias</span></span>
```
Get-AzureRemoteAppProgram [-CollectionName] <String> [[-Alias] <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="6bb17-107">說明</span><span class="sxs-lookup"><span data-stu-id="6bb17-107">DESCRIPTION</span></span>
<span data-ttu-id="6bb17-108">**AzureRemoteAppProgram** Cmdlet 會針對集合檢索一或多個已發佈之 Azure RemoteApp 程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="6bb17-108">The **Get-AzureRemoteAppProgram** cmdlet retrieves the properties of one or more published Azure RemoteApp programs for a collection.</span></span>

## <span data-ttu-id="6bb17-109">示例</span><span class="sxs-lookup"><span data-stu-id="6bb17-109">EXAMPLES</span></span>

### <span data-ttu-id="6bb17-110">範例1：檢索程式的屬性</span><span class="sxs-lookup"><span data-stu-id="6bb17-110">Example 1: Retrieve the properties of a program</span></span>
```
PS C:\> Get-AzureRemoteAppProgram -CollectionName "ContosoApps" -RemoteAppProgram "Finance App"

Alias                : edc85816-4b9e-4284-b3dc-faedb505f5d9

AvailableToUsers     : True

CommandLineArguments : 

IconPngUris          : Microsoft.Azure.Management.RemoteApp.Models.IconPngUrisType

IconUri              : https://liverdcxstorage.blob.core.windows.net/icons/12345678-1234-1234-1234-123412341234.ico?se=2015-03-01T17%3A29%3A51Z&amp;amp;sr=b&amp;amp;sp=r&amp;amp;sig=abcdCCavbcF%2asY4RascaBauishCasd2FasdBHtasd2BPasdi5dasdD

Name                 : Contoso Finance

Status               : Published

VirtualPath          : %SYSTEMDRIVE%\Program Files (x86)\Contoso Finance\Finance.exe
```

<span data-ttu-id="6bb17-111">這個命令會顯示 Azure RemoteApp 程式的屬性。</span><span class="sxs-lookup"><span data-stu-id="6bb17-111">This command displays the properties of an Azure RemoteApp program.</span></span>
<span data-ttu-id="6bb17-112">名為 ContosoApps 的 Azure RemoteApp 集合中有名為「財務 App」的程式。</span><span class="sxs-lookup"><span data-stu-id="6bb17-112">The program, named Finance App, is in the Azure RemoteApp collection named ContosoApps.</span></span>

## <span data-ttu-id="6bb17-113">參數</span><span class="sxs-lookup"><span data-stu-id="6bb17-113">PARAMETERS</span></span>

### <span data-ttu-id="6bb17-114">-別名</span><span class="sxs-lookup"><span data-stu-id="6bb17-114">-Alias</span></span>
<span data-ttu-id="6bb17-115">指定要為其檢索屬性之程式的別名。</span><span class="sxs-lookup"><span data-stu-id="6bb17-115">Specifies the alias of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByAlias
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb17-116">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="6bb17-116">-CollectionName</span></span>
<span data-ttu-id="6bb17-117">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bb17-117">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6bb17-118">-設定檔</span><span class="sxs-lookup"><span data-stu-id="6bb17-118">-Profile</span></span>
<span data-ttu-id="6bb17-119">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="6bb17-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6bb17-120">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="6bb17-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6bb17-121">-RemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="6bb17-121">-RemoteAppProgram</span></span>
<span data-ttu-id="6bb17-122">指定要為其檢索屬性之程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="6bb17-122">Specifies the name of the program for which to retrieve properties.</span></span>

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="6bb17-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb17-123">CommonParameters</span></span>
<span data-ttu-id="6bb17-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6bb17-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb17-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6bb17-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb17-126">輸入</span><span class="sxs-lookup"><span data-stu-id="6bb17-126">INPUTS</span></span>

## <span data-ttu-id="6bb17-127">輸出</span><span class="sxs-lookup"><span data-stu-id="6bb17-127">OUTPUTS</span></span>

## <span data-ttu-id="6bb17-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6bb17-128">NOTES</span></span>

## <span data-ttu-id="6bb17-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6bb17-129">RELATED LINKS</span></span>

[<span data-ttu-id="6bb17-130">發佈-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="6bb17-130">Publish-AzureRemoteAppProgram</span></span>](./Publish-AzureRemoteAppProgram.md)

[<span data-ttu-id="6bb17-131">取消發佈-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="6bb17-131">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


