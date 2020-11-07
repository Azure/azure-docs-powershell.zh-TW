---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967497"
---
# <span data-ttu-id="02def-101">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="02def-101">Set-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="02def-102">摘要</span><span class="sxs-lookup"><span data-stu-id="02def-102">SYNOPSIS</span></span>
<span data-ttu-id="02def-103">設定 Azure RemoteApp 工作區的屬性。</span><span class="sxs-lookup"><span data-stu-id="02def-103">Sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="02def-104">句法</span><span class="sxs-lookup"><span data-stu-id="02def-104">SYNTAX</span></span>

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="02def-105">說明</span><span class="sxs-lookup"><span data-stu-id="02def-105">DESCRIPTION</span></span>
<span data-ttu-id="02def-106">**AzureRemoteAppWorkspace** Cmdlet 會設定 Azure RemoteApp 工作區的屬性。</span><span class="sxs-lookup"><span data-stu-id="02def-106">The **Set-AzureRemoteAppWorkspace** cmdlet sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="02def-107">示例</span><span class="sxs-lookup"><span data-stu-id="02def-107">EXAMPLES</span></span>

### <span data-ttu-id="02def-108">範例1：設定工作區名稱</span><span class="sxs-lookup"><span data-stu-id="02def-108">Example 1: Set the workspace name</span></span>
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

<span data-ttu-id="02def-109">這個命令會將 Azure RemoteApp 工作區名稱設定為 Contoso 工作應用程式。</span><span class="sxs-lookup"><span data-stu-id="02def-109">This command sets the Azure RemoteApp workspace name to Contoso Work Applications.</span></span>

## <span data-ttu-id="02def-110">參數</span><span class="sxs-lookup"><span data-stu-id="02def-110">PARAMETERS</span></span>

### <span data-ttu-id="02def-111">-設定檔</span><span class="sxs-lookup"><span data-stu-id="02def-111">-Profile</span></span>
<span data-ttu-id="02def-112">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="02def-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="02def-113">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="02def-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="02def-114">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="02def-114">-WorkspaceName</span></span>
<span data-ttu-id="02def-115">指定 Azure RemoteApp 工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="02def-115">Specifies the name of the Azure RemoteApp workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02def-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02def-116">CommonParameters</span></span>
<span data-ttu-id="02def-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="02def-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02def-118">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="02def-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02def-119">輸入</span><span class="sxs-lookup"><span data-stu-id="02def-119">INPUTS</span></span>

## <span data-ttu-id="02def-120">輸出</span><span class="sxs-lookup"><span data-stu-id="02def-120">OUTPUTS</span></span>

## <span data-ttu-id="02def-121">筆記</span><span class="sxs-lookup"><span data-stu-id="02def-121">NOTES</span></span>
* <span data-ttu-id="02def-122">在共用工作區中存在指定訂閱的所有 Azure RemoteApp 集合。</span><span class="sxs-lookup"><span data-stu-id="02def-122">All Azure RemoteApp collections for a specified subscription exist within a shared workspace.</span></span>

## <span data-ttu-id="02def-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="02def-123">RELATED LINKS</span></span>

[<span data-ttu-id="02def-124">AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="02def-124">Get-AzureRemoteAppWorkspace</span></span>](./Get-AzureRemoteAppWorkspace.md)


