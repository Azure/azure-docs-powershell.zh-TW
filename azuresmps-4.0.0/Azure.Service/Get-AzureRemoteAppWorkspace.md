---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 035B294E-6A1B-41E9-ACFF-D66F9C1A0B11
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9218862bb1e61abe548a94ed5297a6ce69237d54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967065"
---
# <span data-ttu-id="3ddcf-101">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ddcf-101">Get-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="3ddcf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ddcf-102">SYNOPSIS</span></span>
<span data-ttu-id="3ddcf-103">檢索 Azure RemoteApp 工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3ddcf-103">Retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="3ddcf-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ddcf-104">SYNTAX</span></span>

```
Get-AzureRemoteAppWorkspace [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3ddcf-105">說明</span><span class="sxs-lookup"><span data-stu-id="3ddcf-105">DESCRIPTION</span></span>
<span data-ttu-id="3ddcf-106">**AzureRemoteAppWorkspace** Cmdlet 會檢索 Azure RemoteApp 工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3ddcf-106">The **Get-AzureRemoteAppWorkspace** cmdlet retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="3ddcf-107">示例</span><span class="sxs-lookup"><span data-stu-id="3ddcf-107">EXAMPLES</span></span>

### <span data-ttu-id="3ddcf-108">範例1：檢索工作區的相關資訊</span><span class="sxs-lookup"><span data-stu-id="3ddcf-108">Example 1: Retrieve information about a workspace</span></span>
```
PS C:\> Get-AzureRemoteAppWorkspace
ClientUrl                               EndUserFeedName
---------                               ---------------
https://www.remoteapp.windowsazure.com/ Contoso Work Applications
```

<span data-ttu-id="3ddcf-109">這個命令會檢索 Azure RemoteApp 工作區的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3ddcf-109">This command retrieves information about the Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="3ddcf-110">參數</span><span class="sxs-lookup"><span data-stu-id="3ddcf-110">PARAMETERS</span></span>

### <span data-ttu-id="3ddcf-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3ddcf-111">-Profile</span></span>
<span data-ttu-id="3ddcf-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3ddcf-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ddcf-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3ddcf-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ddcf-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ddcf-114">CommonParameters</span></span>
<span data-ttu-id="3ddcf-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ddcf-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ddcf-116">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3ddcf-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ddcf-117">輸入</span><span class="sxs-lookup"><span data-stu-id="3ddcf-117">INPUTS</span></span>

## <span data-ttu-id="3ddcf-118">輸出</span><span class="sxs-lookup"><span data-stu-id="3ddcf-118">OUTPUTS</span></span>

## <span data-ttu-id="3ddcf-119">筆記</span><span class="sxs-lookup"><span data-stu-id="3ddcf-119">NOTES</span></span>

## <span data-ttu-id="3ddcf-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ddcf-120">RELATED LINKS</span></span>

[<span data-ttu-id="3ddcf-121">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="3ddcf-121">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)


