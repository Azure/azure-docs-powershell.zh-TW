---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothubexportdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHubExportDevice.md
ms.openlocfilehash: 3b04e0598897fb206ca781f4f19d9e8e2ec206dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959759"
---
# <span data-ttu-id="f6353-101">New-AzIotHubExportDevice</span><span class="sxs-lookup"><span data-stu-id="f6353-101">New-AzIotHubExportDevice</span></span>

## <span data-ttu-id="f6353-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f6353-102">SYNOPSIS</span></span>
<span data-ttu-id="f6353-103">建立新的匯出裝置作業。</span><span class="sxs-lookup"><span data-stu-id="f6353-103">Creates a new export devices job.</span></span>

## <span data-ttu-id="f6353-104">句法</span><span class="sxs-lookup"><span data-stu-id="f6353-104">SYNTAX</span></span>

```
New-AzIotHubExportDevice [-ResourceGroupName] <String> [-Name] <String> [-ExportBlobContainerUri] <String>
 [-ExcludeKeys] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6353-105">說明</span><span class="sxs-lookup"><span data-stu-id="f6353-105">DESCRIPTION</span></span>
<span data-ttu-id="f6353-106">為 IotHub 建立新的匯出裝置作業。</span><span class="sxs-lookup"><span data-stu-id="f6353-106">Creates a new export devices job for the IotHub.</span></span>
<span data-ttu-id="f6353-107">這會將所有裝置匯出至指定的容器。</span><span class="sxs-lookup"><span data-stu-id="f6353-107">This will export all the devices to the specified container.</span></span> <span data-ttu-id="f6353-108">請參閱下列文章，瞭解如何產生 SAS URI。</span><span class="sxs-lookup"><span data-stu-id="f6353-108">Refer to the following article on how to generate the SAS URI.</span></span>
<span data-ttu-id="f6353-109"> https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span><span class="sxs-lookup"><span data-stu-id="f6353-109">https://docs.microsoft.com/azure/iot-hub/iot-hub-bulk-identity-mgmt#get-the-container-sas-uri .</span></span>

## <span data-ttu-id="f6353-110">示例</span><span class="sxs-lookup"><span data-stu-id="f6353-110">EXAMPLES</span></span>

### <span data-ttu-id="f6353-111">範例1發出匯出裝置要求的問題。</span><span class="sxs-lookup"><span data-stu-id="f6353-111">Example 1 Issue an export device request.</span></span>
```
PS C:\> New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

<span data-ttu-id="f6353-112">針對 IotHub "myiothub" （不含按鍵）建立新的匯出裝置要求。</span><span class="sxs-lookup"><span data-stu-id="f6353-112">Creates a new export device request for the IotHub "myiothub" excluding the keys.</span></span>

## <span data-ttu-id="f6353-113">參數</span><span class="sxs-lookup"><span data-stu-id="f6353-113">PARAMETERS</span></span>

### <span data-ttu-id="f6353-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6353-114">-DefaultProfile</span></span>
<span data-ttu-id="f6353-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f6353-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6353-116">-ExcludeKeys</span><span class="sxs-lookup"><span data-stu-id="f6353-116">-ExcludeKeys</span></span>
<span data-ttu-id="f6353-117">允許匯出不含金鑰的裝置。</span><span class="sxs-lookup"><span data-stu-id="f6353-117">Allows to export devices without keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6353-118">-ExportBlobContainerUri</span><span class="sxs-lookup"><span data-stu-id="f6353-118">-ExportBlobContainerUri</span></span>
<span data-ttu-id="f6353-119">要將 blob 匯出至的 Uri。</span><span class="sxs-lookup"><span data-stu-id="f6353-119">The Uri to export the blob to.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6353-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6353-120">-Name</span></span>
<span data-ttu-id="f6353-121">IotHub 的名稱</span><span class="sxs-lookup"><span data-stu-id="f6353-121">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6353-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6353-122">-ResourceGroupName</span></span>
<span data-ttu-id="f6353-123">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="f6353-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6353-124">-確認</span><span class="sxs-lookup"><span data-stu-id="f6353-124">-Confirm</span></span>
<span data-ttu-id="f6353-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f6353-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6353-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6353-126">-WhatIf</span></span>
<span data-ttu-id="f6353-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6353-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6353-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6353-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6353-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6353-129">CommonParameters</span></span>
<span data-ttu-id="f6353-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f6353-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6353-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f6353-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6353-132">輸入</span><span class="sxs-lookup"><span data-stu-id="f6353-132">INPUTS</span></span>

### <span data-ttu-id="f6353-133">System.object</span><span class="sxs-lookup"><span data-stu-id="f6353-133">System.String</span></span>

## <span data-ttu-id="f6353-134">輸出</span><span class="sxs-lookup"><span data-stu-id="f6353-134">OUTPUTS</span></span>

### <span data-ttu-id="f6353-135">PSIotHubJobResponse （IotHub.）。</span><span class="sxs-lookup"><span data-stu-id="f6353-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubJobResponse</span></span>

## <span data-ttu-id="f6353-136">筆記</span><span class="sxs-lookup"><span data-stu-id="f6353-136">NOTES</span></span>

## <span data-ttu-id="f6353-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6353-137">RELATED LINKS</span></span>
