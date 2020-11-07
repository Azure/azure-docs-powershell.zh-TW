---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2CBF8DEF-954C-4D9F-B495-C2F76550BC79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f7e8a7a08ac2793b7e4aeb8615e5fb8fc1f727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967061"
---
# <span data-ttu-id="ef4d0-101">Get-AzureRoleSize</span><span class="sxs-lookup"><span data-stu-id="ef4d0-101">Get-AzureRoleSize</span></span>

## <span data-ttu-id="ef4d0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef4d0-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4d0-103">取得目前訂閱的角色大小資訊。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-103">Gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="ef4d0-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef4d0-104">SYNTAX</span></span>

```
Get-AzureRoleSize [[-InstanceSize] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ef4d0-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef4d0-105">DESCRIPTION</span></span>
<span data-ttu-id="ef4d0-106">**AzureRoleSize** Cmdlet 會取得目前訂閱的角色大小資訊。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-106">The **Get-AzureRoleSize** cmdlet gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="ef4d0-107">示例</span><span class="sxs-lookup"><span data-stu-id="ef4d0-107">EXAMPLES</span></span>

### <span data-ttu-id="ef4d0-108">範例1：取得角色大小資訊</span><span class="sxs-lookup"><span data-stu-id="ef4d0-108">Example 1: Get role size information</span></span>
```
PS C:\> Get-AzureRoleSize

          InstanceSize               : A6
          RoleSizeLabel              :
          Cores                      : 4
          MemoryInMb                 : 28672
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="ef4d0-109">這個命令會取得目前訂閱的角色大小資訊。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-109">This command gets role size information for the current subscription.</span></span>

### <span data-ttu-id="ef4d0-110">範例2：取得角色大小資訊並指定角色大小名稱</span><span class="sxs-lookup"><span data-stu-id="ef4d0-110">Example 2: Get role size information and specify the role size name</span></span>
```
PS C:\> Get-AzureRoleSize -InstanceSize A7

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="ef4d0-111">這個命令會取得指定角色大小的角色大小資訊。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-111">This command gets role size information for the specified role size.</span></span>

### <span data-ttu-id="ef4d0-112">範例3：在所有 Azure 服務中取得所有虛擬機器的角色大小資訊</span><span class="sxs-lookup"><span data-stu-id="ef4d0-112">Example 3: Get role size information for all virtual machines in all of the Azure services</span></span>
```
PS C:\> Get-AzureService | Get-AzureVM | Get-AzureRoleSize
```

<span data-ttu-id="ef4d0-113">這個命令會取得所有 Azure 服務中所有虛擬機器的角色大小資訊。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-113">This command gets role size information for all virtual machines in all of the Azure services.</span></span>

## <span data-ttu-id="ef4d0-114">參數</span><span class="sxs-lookup"><span data-stu-id="ef4d0-114">PARAMETERS</span></span>

### <span data-ttu-id="ef4d0-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ef4d0-115">-InformationAction</span></span>
<span data-ttu-id="ef4d0-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ef4d0-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ef4d0-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef4d0-118">持續</span><span class="sxs-lookup"><span data-stu-id="ef4d0-118">Continue</span></span>
- <span data-ttu-id="ef4d0-119">理會</span><span class="sxs-lookup"><span data-stu-id="ef4d0-119">Ignore</span></span>
- <span data-ttu-id="ef4d0-120">看</span><span class="sxs-lookup"><span data-stu-id="ef4d0-120">Inquire</span></span>
- <span data-ttu-id="ef4d0-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ef4d0-121">SilentlyContinue</span></span>
- <span data-ttu-id="ef4d0-122">停止</span><span class="sxs-lookup"><span data-stu-id="ef4d0-122">Stop</span></span>
- <span data-ttu-id="ef4d0-123">封存</span><span class="sxs-lookup"><span data-stu-id="ef4d0-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4d0-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ef4d0-124">-InformationVariable</span></span>
<span data-ttu-id="ef4d0-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4d0-126">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="ef4d0-126">-InstanceSize</span></span>
<span data-ttu-id="ef4d0-127">指定角色大小名稱，例如： ExtraSmall、Small、大型、ExtraLarge、A5、A6、A7。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-127">Specifies the role size name, for example: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4d0-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="ef4d0-128">-Profile</span></span>
<span data-ttu-id="ef4d0-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ef4d0-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef4d0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4d0-131">CommonParameters</span></span>
<span data-ttu-id="ef4d0-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4d0-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef4d0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4d0-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ef4d0-134">INPUTS</span></span>

## <span data-ttu-id="ef4d0-135">輸出</span><span class="sxs-lookup"><span data-stu-id="ef4d0-135">OUTPUTS</span></span>

## <span data-ttu-id="ef4d0-136">筆記</span><span class="sxs-lookup"><span data-stu-id="ef4d0-136">NOTES</span></span>

## <span data-ttu-id="ef4d0-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef4d0-137">RELATED LINKS</span></span>

[<span data-ttu-id="ef4d0-138">AzureRole</span><span class="sxs-lookup"><span data-stu-id="ef4d0-138">Get-AzureRole</span></span>](./Get-AzureRole.md)

[<span data-ttu-id="ef4d0-139">AzureService</span><span class="sxs-lookup"><span data-stu-id="ef4d0-139">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="ef4d0-140">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="ef4d0-140">Get-AzureVM</span></span>](./Get-AzureVM.md)


