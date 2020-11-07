---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968500"
---
# <span data-ttu-id="8b74b-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="8b74b-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="8b74b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8b74b-102">SYNOPSIS</span></span>
<span data-ttu-id="8b74b-103">啟動容器遷移作業，將容器遷移至指定的目的地共用。</span><span class="sxs-lookup"><span data-stu-id="8b74b-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="8b74b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8b74b-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b74b-105">說明</span><span class="sxs-lookup"><span data-stu-id="8b74b-105">DESCRIPTION</span></span>
<span data-ttu-id="8b74b-106">啟動容器遷移作業，將容器遷移至指定的目的地共用。</span><span class="sxs-lookup"><span data-stu-id="8b74b-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="8b74b-107">示例</span><span class="sxs-lookup"><span data-stu-id="8b74b-107">EXAMPLES</span></span>

### <span data-ttu-id="8b74b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8b74b-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="8b74b-109">啟動容器遷移。</span><span class="sxs-lookup"><span data-stu-id="8b74b-109">Starts a container migration.</span></span>

## <span data-ttu-id="8b74b-110">參數</span><span class="sxs-lookup"><span data-stu-id="8b74b-110">PARAMETERS</span></span>

### <span data-ttu-id="8b74b-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b74b-111">-StorageAccountName</span></span>
<span data-ttu-id="8b74b-112">容器所尋找的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8b74b-112">The name of storage account where the container locates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b74b-113">-容器</span><span class="sxs-lookup"><span data-stu-id="8b74b-113">-ContainerName</span></span>
<span data-ttu-id="8b74b-114">要遷移之容器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b74b-114">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b74b-115">-共用名稱</span><span class="sxs-lookup"><span data-stu-id="8b74b-115">-ShareName</span></span>
<span data-ttu-id="8b74b-116">包含指定供遷移之容器之共用的名稱。</span><span class="sxs-lookup"><span data-stu-id="8b74b-116">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="8b74b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b74b-117">-ResourceGroupName</span></span>
<span data-ttu-id="8b74b-118">在其中註冊儲存資源提供者的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8b74b-118">The resource group name in which the storage resource provider was registered under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b74b-119">-FarmName</span><span class="sxs-lookup"><span data-stu-id="8b74b-119">-FarmName</span></span>
<span data-ttu-id="8b74b-120">Farm Id。</span><span class="sxs-lookup"><span data-stu-id="8b74b-120">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b74b-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="8b74b-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="8b74b-122">要遷移之目的地共用的 UNC 路徑。</span><span class="sxs-lookup"><span data-stu-id="8b74b-122">The UNC path of the destination share for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b74b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b74b-123">-AsJob</span></span>
<span data-ttu-id="8b74b-124">執行非同步作業，然後傳回工作物件。</span><span class="sxs-lookup"><span data-stu-id="8b74b-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b74b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="8b74b-125">-Force</span></span>
<span data-ttu-id="8b74b-126">不要要求確認。</span><span class="sxs-lookup"><span data-stu-id="8b74b-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b74b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b74b-127">-WhatIf</span></span>
<span data-ttu-id="8b74b-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8b74b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b74b-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8b74b-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b74b-130">-確認</span><span class="sxs-lookup"><span data-stu-id="8b74b-130">-Confirm</span></span>
<span data-ttu-id="8b74b-131">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8b74b-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b74b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b74b-132">CommonParameters</span></span>
<span data-ttu-id="8b74b-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8b74b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b74b-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8b74b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b74b-135">輸入</span><span class="sxs-lookup"><span data-stu-id="8b74b-135">INPUTS</span></span>

## <span data-ttu-id="8b74b-136">輸出</span><span class="sxs-lookup"><span data-stu-id="8b74b-136">OUTPUTS</span></span>

## <span data-ttu-id="8b74b-137">筆記</span><span class="sxs-lookup"><span data-stu-id="8b74b-137">NOTES</span></span>

## <span data-ttu-id="8b74b-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="8b74b-138">RELATED LINKS</span></span>
