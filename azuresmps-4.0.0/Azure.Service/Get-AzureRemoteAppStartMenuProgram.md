---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: FCDEA955-EB64-4EEA-9F4A-04E2C1F0A831
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83664e8be9241782e42d7ba7634691668ed575f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967761"
---
# <span data-ttu-id="7c0af-101">Get-AzureRemoteAppStartMenuProgram</span><span class="sxs-lookup"><span data-stu-id="7c0af-101">Get-AzureRemoteAppStartMenuProgram</span></span>

## <span data-ttu-id="7c0af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c0af-102">SYNOPSIS</span></span>
<span data-ttu-id="7c0af-103">列出 Azure RemoteApp 集合中的 [開始] 功能表程式。</span><span class="sxs-lookup"><span data-stu-id="7c0af-103">Lists the Start Menu programs in an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="7c0af-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c0af-104">SYNTAX</span></span>

```
Get-AzureRemoteAppStartMenuProgram [-CollectionName] <String> [[-ProgramName] <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7c0af-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c0af-105">DESCRIPTION</span></span>
<span data-ttu-id="7c0af-106">**AzureRemoteAppStartMenuProgram** Cmdlet 會列出 Azure RemoteApp 集合所使用的範本影像中的 [開始] 功能表程式。</span><span class="sxs-lookup"><span data-stu-id="7c0af-106">The **Get-AzureRemoteAppStartMenuProgram** cmdlet lists the Start Menu programs in the template image that an Azure RemoteApp collection uses.</span></span>

## <span data-ttu-id="7c0af-107">示例</span><span class="sxs-lookup"><span data-stu-id="7c0af-107">EXAMPLES</span></span>

### <span data-ttu-id="7c0af-108">範例1：列出集合的 [開始] 功能表程式</span><span class="sxs-lookup"><span data-stu-id="7c0af-108">Example 1: List the Start Menu programs for a collection</span></span>
```
PS C:\> Get-AzureRemoteAppStartMenuProgram -CollectionName "ContosoApps"
```

<span data-ttu-id="7c0af-109">這個命令會傳回 ContosoApps 集合的 [開始] 功能表程式的清單。</span><span class="sxs-lookup"><span data-stu-id="7c0af-109">This command returns the list of Start Menu programs for the ContosoApps collection.</span></span>

## <span data-ttu-id="7c0af-110">參數</span><span class="sxs-lookup"><span data-stu-id="7c0af-110">PARAMETERS</span></span>

### <span data-ttu-id="7c0af-111">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="7c0af-111">-CollectionName</span></span>
<span data-ttu-id="7c0af-112">指定 Azure RemoteApp 集合的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c0af-112">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="7c0af-113">-設定檔</span><span class="sxs-lookup"><span data-stu-id="7c0af-113">-Profile</span></span>
<span data-ttu-id="7c0af-114">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="7c0af-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c0af-115">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="7c0af-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c0af-116">-成</span><span class="sxs-lookup"><span data-stu-id="7c0af-116">-ProgramName</span></span>
<span data-ttu-id="7c0af-117">指定要列出資訊之程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c0af-117">Specifies the name of a program for which to list information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="7c0af-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c0af-118">CommonParameters</span></span>
<span data-ttu-id="7c0af-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c0af-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c0af-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7c0af-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c0af-121">輸入</span><span class="sxs-lookup"><span data-stu-id="7c0af-121">INPUTS</span></span>

## <span data-ttu-id="7c0af-122">輸出</span><span class="sxs-lookup"><span data-stu-id="7c0af-122">OUTPUTS</span></span>

## <span data-ttu-id="7c0af-123">筆記</span><span class="sxs-lookup"><span data-stu-id="7c0af-123">NOTES</span></span>

## <span data-ttu-id="7c0af-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c0af-124">RELATED LINKS</span></span>

[<span data-ttu-id="7c0af-125">AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="7c0af-125">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)


