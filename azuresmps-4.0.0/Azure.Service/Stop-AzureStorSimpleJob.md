---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967458"
---
# <span data-ttu-id="1974e-101">Stop-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="1974e-101">Stop-AzureStorSimpleJob</span></span>

## <span data-ttu-id="1974e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1974e-102">SYNOPSIS</span></span>
<span data-ttu-id="1974e-103">停止 StorSimple 作業。</span><span class="sxs-lookup"><span data-stu-id="1974e-103">Stops a StorSimple job.</span></span>

## <span data-ttu-id="1974e-104">句法</span><span class="sxs-lookup"><span data-stu-id="1974e-104">SYNTAX</span></span>

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1974e-105">說明</span><span class="sxs-lookup"><span data-stu-id="1974e-105">DESCRIPTION</span></span>
<span data-ttu-id="1974e-106">**AzureStorSimpleJob** Cmdlet 會停止日常的 StorSimple 作業。</span><span class="sxs-lookup"><span data-stu-id="1974e-106">The **Stop-AzureStorSimpleJob** cmdlet stops an on-going StorSimple job.</span></span>
<span data-ttu-id="1974e-107">您可以提供實例識別碼或作業名稱來指定作業。</span><span class="sxs-lookup"><span data-stu-id="1974e-107">You can specify a jobs by supplying an instance ID or a job name.</span></span>

## <span data-ttu-id="1974e-108">示例</span><span class="sxs-lookup"><span data-stu-id="1974e-108">EXAMPLES</span></span>

### <span data-ttu-id="1974e-109">範例1：停止裝置的作業</span><span class="sxs-lookup"><span data-stu-id="1974e-109">Example 1: Stop jobs for a device</span></span>
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

<span data-ttu-id="1974e-110">這個命令會使用 **AzureStorSimpleJob** Cmdlet 來取得名為 Device07 之裝置的工作。</span><span class="sxs-lookup"><span data-stu-id="1974e-110">This command gets the jobs for the device named Device07, by using the **Get-AzureStorSimpleJob** cmdlet.</span></span>
<span data-ttu-id="1974e-111">命令會使用管線運算子將作業傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1974e-111">The command passes the jobs to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="1974e-112">目前的 Cmdlet 會停止命令傳遞給它的任何作業。</span><span class="sxs-lookup"><span data-stu-id="1974e-112">The current cmdlet stops any jobs that the command passes to it.</span></span>
<span data-ttu-id="1974e-113">命令會指定 *Force* 參數，因此在停止作業之前，不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1974e-113">The command specifies the *Force* parameter, and, so, it does not prompt you for confirmation before it stops a job.</span></span>

### <span data-ttu-id="1974e-114">範例2：停止特定作業</span><span class="sxs-lookup"><span data-stu-id="1974e-114">Example 2: Stop a specific job</span></span>
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

<span data-ttu-id="1974e-115">這個命令會停止具有指定實例識別碼的作業。</span><span class="sxs-lookup"><span data-stu-id="1974e-115">This command stops the job that has the specified instance ID.</span></span>

## <span data-ttu-id="1974e-116">參數</span><span class="sxs-lookup"><span data-stu-id="1974e-116">PARAMETERS</span></span>

### <span data-ttu-id="1974e-117">-Force</span><span class="sxs-lookup"><span data-stu-id="1974e-117">-Force</span></span>
<span data-ttu-id="1974e-118">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="1974e-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1974e-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="1974e-119">-InstanceId</span></span>
<span data-ttu-id="1974e-120">指定要停止的裝置作業識別碼。</span><span class="sxs-lookup"><span data-stu-id="1974e-120">Specifies the ID of the device job to stop.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1974e-121">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1974e-121">-Profile</span></span>
<span data-ttu-id="1974e-122">指定 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1974e-122">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="1974e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1974e-123">CommonParameters</span></span>
<span data-ttu-id="1974e-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1974e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1974e-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1974e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1974e-126">輸入</span><span class="sxs-lookup"><span data-stu-id="1974e-126">INPUTS</span></span>

### <span data-ttu-id="1974e-127">所有</span><span class="sxs-lookup"><span data-stu-id="1974e-127">None</span></span>

## <span data-ttu-id="1974e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="1974e-128">OUTPUTS</span></span>

### <span data-ttu-id="1974e-129">DeviceJobDetails</span><span class="sxs-lookup"><span data-stu-id="1974e-129">DeviceJobDetails</span></span>
<span data-ttu-id="1974e-130">這個 Cmdlet 會取得這個 Cmdlet 停止的 **DeviceJob** 詳細資料。</span><span class="sxs-lookup"><span data-stu-id="1974e-130">This cmdlet gets details of the **DeviceJob** that this cmdlet stops.</span></span>

## <span data-ttu-id="1974e-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1974e-131">NOTES</span></span>

## <span data-ttu-id="1974e-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1974e-132">RELATED LINKS</span></span>

[<span data-ttu-id="1974e-133">AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="1974e-133">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


