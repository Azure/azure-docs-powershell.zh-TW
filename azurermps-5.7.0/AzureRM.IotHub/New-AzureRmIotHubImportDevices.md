---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothubimportdevices
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHubImportDevices.md
ms.openlocfilehash: 84b8224c83e6455e7f59b8a5fe2b330f34e61ac5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448650"
---
# <span data-ttu-id="9fc2b-101">New-AzureRmIotHubImportDevices</span><span class="sxs-lookup"><span data-stu-id="9fc2b-101">New-AzureRmIotHubImportDevices</span></span>

## <span data-ttu-id="9fc2b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9fc2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc2b-103">建立新的匯入裝置作業。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-103">Creates a new import devices job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fc2b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9fc2b-104">SYNTAX</span></span>

```
New-AzureRmIotHubImportDevices [-ResourceGroupName] <String> [-Name] <String> [-InputBlobContainerUri] <String>
 [-OutputBlobContainerUri] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fc2b-105">說明</span><span class="sxs-lookup"><span data-stu-id="9fc2b-105">DESCRIPTION</span></span>
<span data-ttu-id="9fc2b-106">為 IotHub 建立新的匯入裝置作業。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-106">Creates a new import devices job for the IotHub.</span></span>
<span data-ttu-id="9fc2b-107">這會將所有裝置從指定的容器匯入到 IotHub。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-107">This will import all the devices to the IotHub from the specified container.</span></span> <span data-ttu-id="9fc2b-108">請參閱下列文章，瞭解如何產生 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="9fc2b-109"> https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span><span class="sxs-lookup"><span data-stu-id="9fc2b-109">https://azure.microsoft.com/en-us/documentation/articles/iot-hub-bulk-identity-mgmt/ .</span></span>

## <span data-ttu-id="9fc2b-110">示例</span><span class="sxs-lookup"><span data-stu-id="9fc2b-110">EXAMPLES</span></span>

### <span data-ttu-id="9fc2b-111">範例1</span><span class="sxs-lookup"><span data-stu-id="9fc2b-111">Example 1</span></span>
```
PS C:\> New-AzureRmIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

<span data-ttu-id="9fc2b-112">為 IotHub "myiothub" 建立新的匯入裝置要求。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-112">Creates a new import device request for the IotHub "myiothub".</span></span>

## <span data-ttu-id="9fc2b-113">參數</span><span class="sxs-lookup"><span data-stu-id="9fc2b-113">PARAMETERS</span></span>

### <span data-ttu-id="9fc2b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc2b-114">-DefaultProfile</span></span>
<span data-ttu-id="9fc2b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9fc2b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc2b-116">-InputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="9fc2b-116">-InputBlobContainerUri</span></span>
<span data-ttu-id="9fc2b-117">FileUpload 的輸入 Blob 容器 Uri</span><span class="sxs-lookup"><span data-stu-id="9fc2b-117">Input Blob Container Uri for FileUpload</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc2b-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="9fc2b-118">-Name</span></span>
<span data-ttu-id="9fc2b-119">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="9fc2b-119">Name of the IotHub</span></span>

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

### <span data-ttu-id="9fc2b-120">-OutputBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="9fc2b-120">-OutputBlobContainerUri</span></span>
<span data-ttu-id="9fc2b-121">要寫入輸出的 Uri。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-121">The Uri to write the output to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc2b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc2b-122">-ResourceGroupName</span></span>
<span data-ttu-id="9fc2b-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="9fc2b-123">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9fc2b-124">-確認</span><span class="sxs-lookup"><span data-stu-id="9fc2b-124">-Confirm</span></span>
<span data-ttu-id="9fc2b-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc2b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fc2b-126">-WhatIf</span></span>
<span data-ttu-id="9fc2b-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fc2b-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc2b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc2b-129">CommonParameters</span></span>
<span data-ttu-id="9fc2b-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fc2b-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc2b-132">輸入</span><span class="sxs-lookup"><span data-stu-id="9fc2b-132">INPUTS</span></span>

### <span data-ttu-id="9fc2b-133">System.object</span><span class="sxs-lookup"><span data-stu-id="9fc2b-133">System.String</span></span>

## <span data-ttu-id="9fc2b-134">輸出</span><span class="sxs-lookup"><span data-stu-id="9fc2b-134">OUTPUTS</span></span>

### <span data-ttu-id="9fc2b-135">JobResponse 中的 IotHub。</span><span class="sxs-lookup"><span data-stu-id="9fc2b-135">Microsoft.Azure.Management.IotHub.Models.JobResponse</span></span>

## <span data-ttu-id="9fc2b-136">筆記</span><span class="sxs-lookup"><span data-stu-id="9fc2b-136">NOTES</span></span>

## <span data-ttu-id="9fc2b-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="9fc2b-137">RELATED LINKS</span></span>

