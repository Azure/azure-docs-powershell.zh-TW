---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967768"
---
# <span data-ttu-id="692c1-101">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="692c1-101">Get-AzureRemoteAppOperationResult</span></span>

## <span data-ttu-id="692c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="692c1-102">SYNOPSIS</span></span>
<span data-ttu-id="692c1-103">檢索 Azure RemoteApp 作業的結果。</span><span class="sxs-lookup"><span data-stu-id="692c1-103">Retrieves the result of an Azure RemoteApp operation.</span></span>

## <span data-ttu-id="692c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="692c1-104">SYNTAX</span></span>

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="692c1-105">說明</span><span class="sxs-lookup"><span data-stu-id="692c1-105">DESCRIPTION</span></span>
<span data-ttu-id="692c1-106">**AzureRemoteAppOperationResult** Cmdlet 會檢索長時間執行的 Azure RemoteApp 作業的結果。</span><span class="sxs-lookup"><span data-stu-id="692c1-106">The **Get-AzureRemoteAppOperationResult** cmdlet retrieves the result of a long-running Azure RemoteApp operation.</span></span>
<span data-ttu-id="692c1-107">Azure RemoteApp 針對需要服務處理且無法立即傳回的許多動作，使用長時間執行的作業。</span><span class="sxs-lookup"><span data-stu-id="692c1-107">Azure RemoteApp uses long-running operations for many actions that require processing by the service and cannot return immediately.</span></span>
<span data-ttu-id="692c1-108">傳回追蹤識別碼的 Cmdlet 範例包括 [ **更新-AzureRemoteAppCollection** ]、[ **設定 AzureRemoteAppWorkspace** **]、[中斷連線] AzureRemoteAppSession** 及其他。</span><span class="sxs-lookup"><span data-stu-id="692c1-108">Examples of cmdlets that return tracking IDs include **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** , and others.</span></span>

## <span data-ttu-id="692c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="692c1-109">EXAMPLES</span></span>

### <span data-ttu-id="692c1-110">範例1：使用追蹤識別碼來取得運算結果</span><span class="sxs-lookup"><span data-stu-id="692c1-110">Example 1: Use a tracking ID to get an operation result</span></span>
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

<span data-ttu-id="692c1-111">這個命令會儲存從 Azure RemoteApp 作業傳回的追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="692c1-111">This command saves the tracking ID returned from an Azure RemoteApp operation.</span></span>
<span data-ttu-id="692c1-112">追蹤識別碼會傳遞到下列命令中的 **AzureRemoteAppOperationResult** 。</span><span class="sxs-lookup"><span data-stu-id="692c1-112">The tracking ID is passed to **Get-AzureRemoteAppOperationResult** in the command that follows.</span></span>

## <span data-ttu-id="692c1-113">參數</span><span class="sxs-lookup"><span data-stu-id="692c1-113">PARAMETERS</span></span>

### <span data-ttu-id="692c1-114">-設定檔</span><span class="sxs-lookup"><span data-stu-id="692c1-114">-Profile</span></span>
<span data-ttu-id="692c1-115">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="692c1-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="692c1-116">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="692c1-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="692c1-117">-TrackingId</span><span class="sxs-lookup"><span data-stu-id="692c1-117">-TrackingId</span></span>
<span data-ttu-id="692c1-118">指定作業的追蹤識別碼。</span><span class="sxs-lookup"><span data-stu-id="692c1-118">Specifies the tracking ID of an operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692c1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692c1-119">CommonParameters</span></span>
<span data-ttu-id="692c1-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="692c1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692c1-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="692c1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692c1-122">輸入</span><span class="sxs-lookup"><span data-stu-id="692c1-122">INPUTS</span></span>

## <span data-ttu-id="692c1-123">輸出</span><span class="sxs-lookup"><span data-stu-id="692c1-123">OUTPUTS</span></span>

## <span data-ttu-id="692c1-124">筆記</span><span class="sxs-lookup"><span data-stu-id="692c1-124">NOTES</span></span>

## <span data-ttu-id="692c1-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="692c1-125">RELATED LINKS</span></span>

[<span data-ttu-id="692c1-126">中斷連線-AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="692c1-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="692c1-127">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="692c1-127">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)

[<span data-ttu-id="692c1-128">更新-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="692c1-128">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


