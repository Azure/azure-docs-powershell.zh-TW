---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967998"
---
# <span data-ttu-id="1dff7-101">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="1dff7-101">Get-AzureStorSimpleAccessControlRecord</span></span>

## <span data-ttu-id="1dff7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1dff7-102">SYNOPSIS</span></span>
<span data-ttu-id="1dff7-103">取得服務設定中的存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="1dff7-103">Gets access control records in a service configuration.</span></span>

## <span data-ttu-id="1dff7-104">句法</span><span class="sxs-lookup"><span data-stu-id="1dff7-104">SYNTAX</span></span>

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1dff7-105">說明</span><span class="sxs-lookup"><span data-stu-id="1dff7-105">DESCRIPTION</span></span>
<span data-ttu-id="1dff7-106">**AzureStorSimpleAccessControlRecord** Cmdlet 會取得 StorSimple Manager 服務設定中的存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="1dff7-106">The **Get-AzureStorSimpleAccessControlRecord** cmdlet gets access control records in the StorSimple Manager service configuration.</span></span>
<span data-ttu-id="1dff7-107">這個 Cmdlet 會取得所有記錄或命名記錄。</span><span class="sxs-lookup"><span data-stu-id="1dff7-107">This cmdlet gets all records or a named record.</span></span>

<span data-ttu-id="1dff7-108">存取控制記錄是 iSCSI 啟動器參數的容器。</span><span class="sxs-lookup"><span data-stu-id="1dff7-108">Access control records are containers of iSCSI initiator parameters.</span></span>
<span data-ttu-id="1dff7-109">這些參數指定哪些啟動器可以存取卷。</span><span class="sxs-lookup"><span data-stu-id="1dff7-109">These parameters specify which initiators can access a volume.</span></span>
<span data-ttu-id="1dff7-110">當 iSCSI 啟動器嘗試連線到某個磁片時，裝置會檢查指派給該卷的存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="1dff7-110">When an iSCSI initiator attempts to connect to a volume, your appliance checks the access control records assigned to that volume.</span></span>
<span data-ttu-id="1dff7-111">如果 iSCSI 啟動器參數與對應至該卷的存取控制記錄中的其中一個專案相符，iSCSI 啟動器就可以連線。</span><span class="sxs-lookup"><span data-stu-id="1dff7-111">If the iSCSI initiator parameters match one of the entries in an access control record mapped to that volume, the iSCSI initiator can connect.</span></span>

## <span data-ttu-id="1dff7-112">示例</span><span class="sxs-lookup"><span data-stu-id="1dff7-112">EXAMPLES</span></span>

### <span data-ttu-id="1dff7-113">範例1：取得所有存取控制記錄</span><span class="sxs-lookup"><span data-stu-id="1dff7-113">Example 1: Get all access control records</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

<span data-ttu-id="1dff7-114">這個命令會取得所有存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="1dff7-114">This command gets all access control records.</span></span>

### <span data-ttu-id="1dff7-115">範例2：取得特定的存取控制記錄</span><span class="sxs-lookup"><span data-stu-id="1dff7-115">Example 2: Get a specific access control record</span></span>
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

<span data-ttu-id="1dff7-116">這個命令會取得名為 Acr11 的存取控制記錄。</span><span class="sxs-lookup"><span data-stu-id="1dff7-116">This command gets the access control record named Acr11.</span></span>

## <span data-ttu-id="1dff7-117">參數</span><span class="sxs-lookup"><span data-stu-id="1dff7-117">PARAMETERS</span></span>

### <span data-ttu-id="1dff7-118">-ACRName</span><span class="sxs-lookup"><span data-stu-id="1dff7-118">-ACRName</span></span>
<span data-ttu-id="1dff7-119">指定要取得的存取控制記錄的名稱。</span><span class="sxs-lookup"><span data-stu-id="1dff7-119">Specifies the name of an access control record to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dff7-120">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1dff7-120">-Profile</span></span>
<span data-ttu-id="1dff7-121">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1dff7-121">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="1dff7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dff7-122">CommonParameters</span></span>
<span data-ttu-id="1dff7-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1dff7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dff7-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1dff7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dff7-125">輸入</span><span class="sxs-lookup"><span data-stu-id="1dff7-125">INPUTS</span></span>

### <span data-ttu-id="1dff7-126">所有</span><span class="sxs-lookup"><span data-stu-id="1dff7-126">None</span></span>

## <span data-ttu-id="1dff7-127">輸出</span><span class="sxs-lookup"><span data-stu-id="1dff7-127">OUTPUTS</span></span>

### <span data-ttu-id="1dff7-128">AccessControlRecord、IList\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="1dff7-128">AccessControlRecord, IList\<AccessControlRecord\></span></span>
<span data-ttu-id="1dff7-129">這個 Cmdlet 會傳回 **AccessControlRecord** 物件或 **IList \<AccessControlRecord\>** 物件。</span><span class="sxs-lookup"><span data-stu-id="1dff7-129">This cmdlet returns an **AccessControlRecord** object or an **IList\<AccessControlRecord\>** object.</span></span>
<span data-ttu-id="1dff7-130">**AccessControlRecord** 物件包含下欄欄位：</span><span class="sxs-lookup"><span data-stu-id="1dff7-130">An **AccessControlRecord** object contains the following fields:</span></span> 

- <span data-ttu-id="1dff7-131">**GlobalId** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="1dff7-131">**GlobalId** ( **String** )</span></span> 
- <span data-ttu-id="1dff7-132">**InitiatorName** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="1dff7-132">**InitiatorName** ( **String** )</span></span> 
- <span data-ttu-id="1dff7-133">**InstanceId** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="1dff7-133">**InstanceId** ( **String** )</span></span> 
- <span data-ttu-id="1dff7-134">**名稱** ( **字串** ) </span><span class="sxs-lookup"><span data-stu-id="1dff7-134">**Name** ( **String** )</span></span> 
- <span data-ttu-id="1dff7-135">**OperationInProgress** ( **OperationInProgress** ) </span><span class="sxs-lookup"><span data-stu-id="1dff7-135">**OperationInProgress** ( **OperationInProgress** )</span></span> 
- <span data-ttu-id="1dff7-136">**VolumeCount** ( **int** ) </span><span class="sxs-lookup"><span data-stu-id="1dff7-136">**VolumeCount** ( **int** )</span></span>

## <span data-ttu-id="1dff7-137">筆記</span><span class="sxs-lookup"><span data-stu-id="1dff7-137">NOTES</span></span>

## <span data-ttu-id="1dff7-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="1dff7-138">RELATED LINKS</span></span>

[<span data-ttu-id="1dff7-139">新-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="1dff7-139">New-AzureStorSimpleAccessControlRecord</span></span>](./New-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="1dff7-140">移除-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="1dff7-140">Remove-AzureStorSimpleAccessControlRecord</span></span>](./Remove-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="1dff7-141">Set-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="1dff7-141">Set-AzureStorSimpleAccessControlRecord</span></span>](./Set-AzureStorSimpleAccessControlRecord.md)


