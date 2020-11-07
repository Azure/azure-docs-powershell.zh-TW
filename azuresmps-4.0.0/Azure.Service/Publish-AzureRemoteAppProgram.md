---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: F101382E-B015-4913-B4A0-8827EC423319
online version: ''
schema: 2.0.0
ms.openlocfilehash: b37c4bf3ad2c2aaf74f268b18d17b6af71f4f2fc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967330"
---
# <span data-ttu-id="3f46b-101">Publish-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="3f46b-101">Publish-AzureRemoteAppProgram</span></span>

## <span data-ttu-id="3f46b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3f46b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f46b-103">發佈 Azure RemoteApp 程式。</span><span class="sxs-lookup"><span data-stu-id="3f46b-103">Publishes an Azure RemoteApp program.</span></span>

## <span data-ttu-id="3f46b-104">句法</span><span class="sxs-lookup"><span data-stu-id="3f46b-104">SYNTAX</span></span>

### <span data-ttu-id="3f46b-105">[應用程式識別碼] (預設) </span><span class="sxs-lookup"><span data-stu-id="3f46b-105">App Id (Default)</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-StartMenuAppId] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="3f46b-106">App 路徑</span><span class="sxs-lookup"><span data-stu-id="3f46b-106">App Path</span></span>
```
Publish-AzureRemoteAppProgram [-CollectionName] <String> [-FileVirtualPath] <String> [-CommandLine <String>]
 [-DisplayName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f46b-107">說明</span><span class="sxs-lookup"><span data-stu-id="3f46b-107">DESCRIPTION</span></span>
<span data-ttu-id="3f46b-108">**AzureRemoteAppProgram** Cmdlet 會發佈 azure remoteapp 程式，使其可供 Azure remoteapp 集合的使用者使用。</span><span class="sxs-lookup"><span data-stu-id="3f46b-108">The **Publish-AzureRemoteAppProgram** cmdlet publishes an Azure RemoteApp program, which makes it available to users of the Azure RemoteApp collection.</span></span>

## <span data-ttu-id="3f46b-109">示例</span><span class="sxs-lookup"><span data-stu-id="3f46b-109">EXAMPLES</span></span>

### <span data-ttu-id="3f46b-110">範例1：發佈集合中的程式</span><span class="sxs-lookup"><span data-stu-id="3f46b-110">Example 1: Publish a program in a collection</span></span>
```
PS C:\> Publish-AzureRemoteAppProgram -CollectionName "ContosoApps" -StartMenuAppId "a3732322-89a5-4cbc-9844-9634c74d337f" -DisplayName "Finance App"
```

<span data-ttu-id="3f46b-111">這個命令會在 ContosoApps 集合中發佈程式，並使用指定的 *StartMenuAppId* 將程式新增至 [開始] 功能表。</span><span class="sxs-lookup"><span data-stu-id="3f46b-111">This command publishes the program in the ContosoApps collection with the specified *StartMenuAppId* to add the program to the Start Menu.</span></span>
<span data-ttu-id="3f46b-112">已發佈的應用程式將會顯示名稱 "財務應用程式"。</span><span class="sxs-lookup"><span data-stu-id="3f46b-112">The published app will have a display name of "Finance App".</span></span>

## <span data-ttu-id="3f46b-113">參數</span><span class="sxs-lookup"><span data-stu-id="3f46b-113">PARAMETERS</span></span>

### <span data-ttu-id="3f46b-114">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="3f46b-114">-CollectionName</span></span>
<span data-ttu-id="3f46b-115">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f46b-115">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="3f46b-116">-命令列</span><span class="sxs-lookup"><span data-stu-id="3f46b-116">-CommandLine</span></span>
<span data-ttu-id="3f46b-117">指定此 Cmdlet 發佈之程式的命令列引數。</span><span class="sxs-lookup"><span data-stu-id="3f46b-117">Specifies command-line arguments for the program that this cmdlet publishes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f46b-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3f46b-118">-DisplayName</span></span>
<span data-ttu-id="3f46b-119">指定 Azure RemoteApp 程式的方便使用顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="3f46b-119">Specifies the user-friendly display name of the Azure RemoteApp program.</span></span>
<span data-ttu-id="3f46b-120">使用者會看到此應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="3f46b-120">Users see this as the name of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f46b-121">-FileVirtualPath</span><span class="sxs-lookup"><span data-stu-id="3f46b-121">-FileVirtualPath</span></span>
<span data-ttu-id="3f46b-122">指定程式範本影像內的程式路徑。</span><span class="sxs-lookup"><span data-stu-id="3f46b-122">Specifies the path of the program within the template image of the program.</span></span>

```yaml
Type: String
Parameter Sets: App Path
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f46b-123">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3f46b-123">-Profile</span></span>
<span data-ttu-id="3f46b-124">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3f46b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f46b-125">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3f46b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f46b-126">-StartMenuAppId</span><span class="sxs-lookup"><span data-stu-id="3f46b-126">-StartMenuAppId</span></span>
<span data-ttu-id="3f46b-127">指定此 Cmdlet 用來將程式新增到 [開始] 功能表的 GUID。</span><span class="sxs-lookup"><span data-stu-id="3f46b-127">Specifies a GUID that this cmdlet uses to add the program to the Start Menu.</span></span>

```yaml
Type: String
Parameter Sets: App Id
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f46b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f46b-128">CommonParameters</span></span>
<span data-ttu-id="3f46b-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3f46b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f46b-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3f46b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f46b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="3f46b-131">INPUTS</span></span>

## <span data-ttu-id="3f46b-132">輸出</span><span class="sxs-lookup"><span data-stu-id="3f46b-132">OUTPUTS</span></span>

## <span data-ttu-id="3f46b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3f46b-133">NOTES</span></span>

## <span data-ttu-id="3f46b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f46b-134">RELATED LINKS</span></span>

[<span data-ttu-id="3f46b-135">AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="3f46b-135">Get-AzureRemoteAppProgram</span></span>](./Get-AzureRemoteAppProgram.md)

[<span data-ttu-id="3f46b-136">取消發佈-AzureRemoteAppProgram</span><span class="sxs-lookup"><span data-stu-id="3f46b-136">Unpublish-AzureRemoteAppProgram</span></span>](./Unpublish-AzureRemoteAppProgram.md)


